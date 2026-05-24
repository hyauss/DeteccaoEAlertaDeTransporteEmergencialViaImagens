# Indentificação
        INTEGRANTES	

        Gabriel Barros Albertini - 10419482
        Rafael de Menezes Ros - 10417954
        Vinicius Alves Marques - 10417880
        Felipe do Nascimento Fonseca - 10409389
# Síntese do conteúdo do arquivo
        Exclusão de classes indesejadas
# Código
        import yaml
        import os

        # Caminho para o arquivo data.yaml original
        original_file_path = '/content/-Emergency-Vehicle-Detection--1/data.yaml'
        # Caminho para o novo arquivo data.yaml modificado
        modified_file_path = '/content/-Emergency-Vehicle-Detection--1/data_modified.yaml'

        # Classes a serem removidas
        classes_to_remove = ['Fire Engine', 'Police Vehicle']

        # Carregar o arquivo YAML original
        with open(original_file_path, 'r') as file:
            data = yaml.safe_load(file)

        # Modificar a lista de nomes e o número de classes (nc)
        if 'names' in data and 'nc' in data:
            original_names = data['names']
            new_names = [name for name in original_names if name not in classes_to_remove]
            data['names'] = new_names
            data['nc'] = len(new_names)
            print(f"Classes originais: {original_names}")
            print(f"Novas classes: {new_names}")
            print(f"Novo número de classes (nc): {data['nc']}")
        else:
            print("As chaves 'names' ou 'nc' não foram encontradas no arquivo YAML.")

        # Salvar o arquivo YAML modificado
        with open(modified_file_path, 'w') as file:
            yaml.dump(data, file, default_flow_style=False)

        print(f"Arquivo YAML modificado salvo em: {modified_file_path}")

        # Exibir o cabeçalho do novo arquivo para verificação
        !head {modified_file_path}
# Resultado
        Classes originais: ['Ambulance', 'Fire Engine', 'Police Vehicle']
        Novas classes: ['Ambulance']
        Novo número de classes (nc): 1
        Arquivo YAML modificado salvo em: /content/-Emergency-Vehicle-Detection--1/data_modified.yaml
        names:
        - Ambulance
        nc: 1
        roboflow:
        license: Public Domain
        project: emergency-vehicle-detection-yz9lm-xzev5-ugyzm
        url: https://universe.roboflow.com/viniciuss-workspace-tembs/emergency-vehicle-detection-yz9lm-xzev5-ugyzm/dataset/1
        version: 1
        workspace: viniciuss-workspace-tembs
        test: ../test/images