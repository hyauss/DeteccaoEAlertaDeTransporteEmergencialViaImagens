# Indentificação
        INTEGRANTES

        Gabriel Barros Albertini - 10419482
        Rafael de Menezes Ros - 10417954
        Vinicius Alves Marques - 10417880
        Felipe do Nascimento Fonseca - 10409389
# Síntese do conteúdo do arquivo
        Verificar se o caminho do arquivo gerado em .avi existe e mostrar os conteúdos contidos onde ele deveria estar.
# Código
        import os

        video_path = "/content/runs/detect/predict/https___www.youtube.avi"

        if os.path.exists(video_path):
        print(f"O arquivo de vídeo '{video_path}' existe.")
        else:
        print(f"ATENÇÃO: O arquivo de vídeo '{video_path}' NÃO foi encontrado.")

        # Listar o conteúdo do diretório para verificar os arquivos salvos
        !ls -lh /content/runs/detect/predict/

# Resultado
        import os

        video_path = "/content/runs/detect/predict/https___www.youtube.avi"

        if os.path.exists(video_path):
        print(f"O arquivo de vídeo '{video_path}' existe.")
        else:
        print(f"ATENÇÃO: O arquivo de vídeo '{video_path}' NÃO foi encontrado.")

        # Listar o conteúdo do diretório para verificar os arquivos salvos
        !ls -lh /content/runs/detect/predict/