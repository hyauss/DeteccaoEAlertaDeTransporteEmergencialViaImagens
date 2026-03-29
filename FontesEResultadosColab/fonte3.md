# Indentificação
        INTEGRANTES	

        Gabriel Barros Albertini - 10419482
        Rafael de Menezes Ros - 10417954
        Vinicius Alves Marques - 10417880
        Felipe do Nascimento Fonseca - 10409389
# Codigo
        !pip install roboflow

        from roboflow import Roboflow
        rf = Roboflow(api_key="XXXXXXXXXXXX")
        project = rf.workspace("viniciuss-workspace-tembs").project("emergency-vehicle-detection-yz9lm-xzev5-ugyzm")
        version = project.version(1)
        dataset = version.download("yolov8")
# Resultado
        Requirement already satisfied: roboflow in /usr/local/lib/python3.12/dist-packages (1.2.16)
        Requirement already satisfied: certifi in /usr/local/lib/python3.12/dist-packages (from roboflow) (2026.2.25)
        Requirement already satisfied: idna==3.7 in /usr/local/lib/python3.12/dist-packages (from roboflow) (3.7)
        Requirement already satisfied: cycler in /usr/local/lib/python3.12/dist-packages (from roboflow) (0.12.1)
        Requirement already satisfied: kiwisolver>=1.3.1 in /usr/local/lib/python3.12/dist-packages (from roboflow) (1.5.0)
        Requirement already satisfied: matplotlib in /usr/local/lib/python3.12/dist-packages (from roboflow) (3.10.0)
        Requirement already satisfied: numpy>=1.18.5 in /usr/local/lib/python3.12/dist-packages (from roboflow) (2.0.2)
        Requirement already satisfied: opencv-python-headless==4.10.0.84 in /usr/local/lib/python3.12/dist-packages (from roboflow) (4.10.0.84)
        Requirement already satisfied: Pillow>=7.1.2 in /usr/local/lib/python3.12/dist-packages (from roboflow) (11.3.0)
        Requirement already satisfied: pillow-avif-plugin<2 in /usr/local/lib/python3.12/dist-packages (from roboflow) (1.5.5)
        Requirement already satisfied: python-dateutil in /usr/local/lib/python3.12/dist-packages (from roboflow) (2.9.0.post0)
        Requirement already satisfied: python-dotenv in /usr/local/lib/python3.12/dist-packages (from roboflow) (1.2.2)
        Requirement already satisfied: requests in /usr/local/lib/python3.12/dist-packages (from roboflow) (2.32.4)
        Requirement already satisfied: six in /usr/local/lib/python3.12/dist-packages (from roboflow) (1.17.0)
        Requirement already satisfied: urllib3>=1.26.6 in /usr/local/lib/python3.12/dist-packages (from roboflow) (2.5.0)
        Requirement already satisfied: tqdm>=4.41.0 in /usr/local/lib/python3.12/dist-packages (from roboflow) (4.67.3)
        Requirement already satisfied: PyYAML>=5.3.1 in /usr/local/lib/python3.12/dist-packages (from roboflow) (6.0.3)
        Requirement already satisfied: requests-toolbelt in /usr/local/lib/python3.12/dist-packages (from roboflow) (1.0.0)
        Requirement already satisfied: filetype in /usr/local/lib/python3.12/dist-packages (from roboflow) (1.2.0)
        Requirement already satisfied: pi-heif<2 in /usr/local/lib/python3.12/dist-packages (from roboflow) (1.3.0)
        Requirement already satisfied: contourpy>=1.0.1 in /usr/local/lib/python3.12/dist-packages (from matplotlib->roboflow) (1.3.3)
        Requirement already satisfied: fonttools>=4.22.0 in /usr/local/lib/python3.12/dist-packages (from matplotlib->roboflow) (4.62.1)
        Requirement already satisfied: packaging>=20.0 in /usr/local/lib/python3.12/dist-packages (from matplotlib->roboflow) (26.0)
        Requirement already satisfied: pyparsing>=2.3.1 in /usr/local/lib/python3.12/dist-packages (from matplotlib->roboflow) (3.3.2)
        Requirement already satisfied: charset_normalizer<4,>=2 in /usr/local/lib/python3.12/dist-packages (from requests->roboflow) (3.4.6)
        loading Roboflow workspace...
        loading Roboflow project...
        Downloading Dataset Version Zip in -Emergency-Vehicle-Detection--1 to yolov8:: 100%|██████████| 327267/327267 [00:05<00:00, 61252.70it/s]

        Extracting Dataset Version Zip to -Emergency-Vehicle-Detection--1 in yolov8:: 100%|██████████| 13536/13536 [00:01<00:00, 7036.83it/s]
        Creating new Ultralytics Settings v0.0.6 file ✅ 
        View Ultralytics Settings with 'yolo settings' or at '/root/.config/Ultralytics/settings.json'
        Update Settings with 'yolo settings key=value', i.e. 'yolo settings runs_dir=path/to/dir'. For help see https://docs.ultralytics.com/quickstart/#ultralytics-settings.

