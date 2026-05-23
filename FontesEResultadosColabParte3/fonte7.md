# Indentificação
        INTEGRANTES	

        Gabriel Barros Albertini - 10419482
        Rafael de Menezes Ros - 10417954
        Vinicius Alves Marques - 10417880
        Felipe do Nascimento Fonseca - 10409389
# Síntese do conteúdo do arquivo
        Sobrescrever os arquivos de labels originais com as classes filtradas e re-indexadas.
# Código
        import yaml
        import os

        # Caminhos dos arquivos YAML
        original_data_yaml_path = '/content/-Emergency-Vehicle-Detection--1/data.yaml'
        modified_data_yaml_path = '/content/-Emergency-Vehicle-Detection--1/data_modified.yaml'

        # Diretório base do dataset
        base_dataset_dir = '/content/-Emergency-Vehicle-Detection--1'

        # Carregar o data.yaml original para mapear os IDs das classes originais para seus nomes
        with open(original_data_yaml_path, 'r') as f:
            original_data = yaml.safe_load(f)
        original_class_names = original_data.get('names', [])
        original_name_to_id = {name: i for i, name in enumerate(original_class_names)}

        # Carregar o data_modified.yaml para obter os novos nomes e IDs das classes
        with open(modified_data_yaml_path, 'r') as f:
            modified_data = yaml.safe_load(f)
        new_class_names = modified_data.get('names', [])
        new_name_to_id = {name: i for i, name in enumerate(new_class_names)}

        print(f"Classes originais: {original_class_names}")
        print(f"Novas classes: {new_class_names}\n")

        # Diretórios de labels a serem processados
        label_subdirs = ['train/labels', 'valid/labels', 'test/labels']

        print("ATENÇÃO: Este script irá sobrescrever os arquivos de labels originais com as classes filtradas e re-indexadas.")

        for subdir in label_subdirs:
            label_dir = os.path.join(base_dataset_dir, subdir)
            
            if not os.path.exists(label_dir):
                print(f"Diretório de labels não encontrado: {label_dir}. Pulando...")
                continue

            print(f"Processando labels em: {label_dir}")

            for filename in os.listdir(label_dir):
                if filename.endswith('.txt'):
                    file_path = os.path.join(label_dir, filename)
                    
                    filtered_lines = []
                    with open(file_path, 'r') as f:
                        lines = f.readlines()
                    
                    for line in lines:
                        parts = line.strip().split()
                        if len(parts) < 5: # Verifica se a linha tem o formato esperado
                            print(f"Aviso: Linha malformada em {filename}, pulando: {line.strip()}")
                            continue
                        
                        try:
                            original_class_id = int(parts[0])
                            if original_class_id < 0 or original_class_id >= len(original_class_names):
                                print(f"Aviso: ID de classe inválido {original_class_id} em {filename}, pulando linha: {line.strip()}")
                                continue

                            class_name = original_class_names[original_class_id]

                            if class_name in new_class_names:
                                new_class_id = new_name_to_id[class_name]
                                filtered_lines.append(f"{new_class_id} {' '.join(parts[1:])}\n")
                        except ValueError:
                            print(f"Aviso: Erro de conversão em {filename}, pulando linha: {line.strip()}")
                            continue

                    # Sobrescreve o arquivo com as linhas filtradas e re-indexadas
                    with open(file_path, 'w') as f:
                        f.writelines(filtered_lines)
            print(f"Finalizado o processamento de labels em {label_dir}.\n")

        print("Todos os arquivos de labels foram atualizados. Você pode agora tentar treinar o modelo novamente.")
# Resultado
        Classes originais: ['Ambulance', 'Fire Engine', 'Police Vehicle']
        Novas classes: ['Ambulance']

        ATENÇÃO: Este script irá sobrescrever os arquivos de labels originais com as classes filtradas e re-indexadas.
        Processando labels em: /content/-Emergency-Vehicle-Detection--1/train/labels
        Finalizado o processamento de labels em /content/-Emergency-Vehicle-Detection--1/train/labels.

        Processando labels em: /content/-Emergency-Vehicle-Detection--1/valid/labels
        Finalizado o processamento de labels em /content/-Emergency-Vehicle-Detection--1/valid/labels.

        Processando labels em: /content/-Emergency-Vehicle-Detection--1/test/labels
        Finalizado o processamento de labels em /content/-Emergency-Vehicle-Detection--1/test/labels.

        Todos os arquivos de labels foram atualizados. Você pode agora tentar treinar o modelo novamente.