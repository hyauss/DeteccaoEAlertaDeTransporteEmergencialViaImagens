# Indentificação
        INTEGRANTES	

        Gabriel Barros Albertini - 10419482
        Rafael de Menezes Ros - 10417954
        Vinicius Alves Marques - 10417880
        Felipe do Nascimento Fonseca - 10409389
# Síntese do conteúdo do arquivo
        Processar um vídeo fonte (source) com o modelo treinado.
# Código
    from ultralytics import YOLO

    # carregar modelo treinado
    model = YOLO("/content/runs/detect/train/weights/best.pt")

    # processar vídeo
    results = model.predict(
        #Altere source para mudar o vídeo processado.
        #A reslução deve ser no mínimo 1080p
        source="https://www.youtube.com/watch?v=vxR6dJjssrs",
        imgsz=640,
        conf=0.5,
        save=True
    )

    print("Detecção finalizada.")
# Resultado

    requirements: Ultralytics requirement ['pytubefix>=6.5.2'] not found, attempting AutoUpdate...
    Using Python 3.12.13 environment at: /usr
    Resolved 12 packages in 480ms
    Prepared 2 packages in 1.45s
    Installed 2 packages in 108ms
    + nodejs-wheel-binaries==24.15.0
    + pytubefix==10.7.2

    requirements: AutoUpdate success ✅ 2.5s
    WARNING ⚠️ requirements: Restart runtime or rerun command for updates to take effect

    1/1: https://www.youtube.com/watch?v=vxR6dJjssrs... Success ✅ (1446 frames of shape 1920x1080 at 29.97 FPS)

    WARNING ⚠️ 
    Inference results will accumulate in RAM unless `stream=True` is passed, which can cause out-of-memory errors for large
    sources or long-running streams and videos. See https://docs.ultralytics.com/modes/predict/ for help.

    Example:
        results = model(source=..., stream=True)  # generator of Results objects
        for r in results:
            boxes = r.boxes  # Boxes object for bbox outputs
            masks = r.masks  # Masks object for segment masks outputs
            probs = r.probs  # Class probabilities for classification outputs

    0: 384x640 (no detections), 255.0ms
    0: 384x640 (no detections), 12.1ms
    0: 384x640 (no detections), 14.4ms
    0: 384x640 (no detections), 7.6ms
    0: 384x640 (no detections), 11.7ms
    0: 384x640 (no detections), 10.6ms
    0: 384x640 (no detections), 10.3ms
    0: 384x640 (no detections), 6.7ms
    0: 384x640 (no detections), 17.6ms
    0: 384x640 (no detections), 6.6ms
    0: 384x640 (no detections), 10.2ms
    0: 384x640 (no detections), 7.2ms
    0: 384x640 (no detections), 6.4ms
    0: 384x640 (no detections), 13.6ms
    0: 384x640 (no detections), 7.2ms
    0: 384x640 (no detections), 7.0ms
    0: 384x640 (no detections), 9.8ms
    0: 384x640 (no detections), 23.3ms
    0: 384x640 (no detections), 16.7ms
    0: 384x640 (no detections), 11.5ms
    0: 384x640 (no detections), 15.9ms
    0: 384x640 (no detections), 7.7ms
    0: 384x640 (no detections), 12.6ms
    0: 384x640 (no detections), 10.6ms
    0: 384x640 (no detections), 11.3ms
    0: 384x640 (no detections), 10.0ms
    0: 384x640 (no detections), 13.2ms
    0: 384x640 (no detections), 36.9ms
    0: 384x640 (no detections), 11.6ms
    0: 384x640 (no detections), 18.6ms
    0: 384x640 (no detections), 16.9ms
    0: 384x640 (no detections), 8.6ms
    0: 384x640 (no detections), 35.2ms
    0: 384x640 (no detections), 24.3ms
    0: 384x640 (no detections), 35.9ms
    0: 384x640 (no detections), 29.8ms
    0: 384x640 (no detections), 25.9ms
    0: 384x640 (no detections), 19.9ms
    0: 384x640 (no detections), 28.6ms
    0: 384x640 (no detections), 27.5ms
    0: 384x640 (no detections), 30.3ms
    0: 384x640 (no detections), 26.7ms
    0: 384x640 (no detections), 33.5ms
    0: 384x640 (no detections), 35.6ms
    0: 384x640 (no detections), 11.5ms
    0: 384x640 (no detections), 17.3ms
    0: 384x640 (no detections), 25.0ms
    0: 384x640 1 Ambulance, 26.1ms
    0: 384x640 (no detections), 37.6ms
    0: 384x640 (no detections), 12.0ms
    0: 384x640 (no detections), 17.0ms
    0: 384x640 (no detections), 11.5ms
    0: 384x640 (no detections), 17.9ms
    0: 384x640 (no detections), 20.4ms
    0: 384x640 (no detections), 10.5ms
    0: 384x640 (no detections), 10.6ms
    0: 384x640 (no detections), 10.5ms
    0: 384x640 (no detections), 17.0ms
    0: 384x640 (no detections), 11.6ms
    0: 384x640 (no detections), 10.1ms
    0: 384x640 (no detections), 10.2ms
    0: 384x640 (no detections), 10.1ms
    0: 384x640 (no detections), 10.6ms
    0: 384x640 (no detections), 11.3ms
    0: 384x640 (no detections), 12.8ms
    0: 384x640 (no detections), 9.6ms
    0: 384x640 (no detections), 11.1ms
    0: 384x640 (no detections), 31.0ms
    0: 384x640 (no detections), 10.8ms
    0: 384x640 (no detections), 9.3ms
    0: 384x640 (no detections), 9.6ms
    0: 384x640 (no detections), 9.3ms
    0: 384x640 (no detections), 7.6ms
    0: 384x640 (no detections), 10.0ms
    0: 384x640 (no detections), 7.7ms
    0: 384x640 (no detections), 7.9ms
    0: 384x640 (no detections), 10.1ms
    0: 384x640 (no detections), 12.5ms
    0: 384x640 (no detections), 10.1ms
    0: 384x640 (no detections), 9.8ms
    0: 384x640 (no detections), 9.6ms
    0: 384x640 (no detections), 9.2ms
    0: 384x640 (no detections), 11.8ms
    0: 384x640 (no detections), 9.6ms
    0: 384x640 (no detections), 11.7ms
    0: 384x640 1 Ambulance, 12.5ms
    0: 384x640 (no detections), 6.9ms
    0: 384x640 (no detections), 12.4ms
    0: 384x640 (no detections), 9.3ms
    0: 384x640 (no detections), 15.4ms
    0: 384x640 (no detections), 10.8ms
    0: 384x640 (no detections), 9.6ms
    0: 384x640 (no detections), 9.9ms
    0: 384x640 (no detections), 10.1ms
    0: 384x640 (no detections), 6.9ms
    0: 384x640 (no detections), 16.4ms
    0: 384x640 (no detections), 12.5ms
    0: 384x640 (no detections), 8.3ms
    0: 384x640 (no detections), 11.7ms
    0: 384x640 (no detections), 7.3ms
    0: 384x640 (no detections), 7.2ms
    0: 384x640 (no detections), 17.8ms
    0: 384x640 (no detections), 17.7ms
    0: 384x640 (no detections), 10.1ms
    0: 384x640 (no detections), 13.0ms
    0: 384x640 (no detections), 12.0ms
    0: 384x640 (no detections), 11.8ms
    0: 384x640 (no detections), 16.1ms
    0: 384x640 (no detections), 21.5ms
    0: 384x640 (no detections), 14.5ms
    0: 384x640 (no detections), 16.4ms
    0: 384x640 (no detections), 11.5ms
    0: 384x640 (no detections), 6.8ms
    0: 384x640 (no detections), 13.4ms
    0: 384x640 (no detections), 10.3ms
    0: 384x640 (no detections), 9.7ms
    0: 384x640 (no detections), 16.8ms
    0: 384x640 (no detections), 22.3ms
    0: 384x640 (no detections), 13.8ms
    0: 384x640 (no detections), 10.4ms
    0: 384x640 (no detections), 9.8ms
    0: 384x640 (no detections), 10.9ms
    0: 384x640 (no detections), 10.6ms
    0: 384x640 (no detections), 11.3ms
    0: 384x640 (no detections), 10.9ms
    0: 384x640 (no detections), 11.1ms
    0: 384x640 (no detections), 19.9ms
    0: 384x640 (no detections), 20.4ms
    0: 384x640 (no detections), 11.0ms
    0: 384x640 (no detections), 11.4ms
    0: 384x640 (no detections), 10.3ms
    0: 384x640 (no detections), 10.5ms
    0: 384x640 (no detections), 9.8ms
    0: 384x640 (no detections), 15.6ms
    0: 384x640 (no detections), 10.7ms
    0: 384x640 (no detections), 6.8ms
    0: 384x640 (no detections), 14.4ms
    0: 384x640 (no detections), 10.0ms
    0: 384x640 (no detections), 11.6ms
    0: 384x640 (no detections), 13.0ms
    0: 384x640 (no detections), 9.6ms
    0: 384x640 (no detections), 19.1ms
    0: 384x640 (no detections), 10.2ms
    0: 384x640 (no detections), 14.1ms
    0: 384x640 (no detections), 13.7ms
    0: 384x640 (no detections), 13.1ms
    0: 384x640 (no detections), 10.4ms
    0: 384x640 (no detections), 12.0ms
    0: 384x640 (no detections), 9.1ms
    0: 384x640 (no detections), 18.6ms
    0: 384x640 (no detections), 11.0ms
    0: 384x640 (no detections), 12.5ms
    0: 384x640 (no detections), 10.5ms
    0: 384x640 (no detections), 16.1ms
    0: 384x640 (no detections), 10.0ms
    0: 384x640 (no detections), 8.8ms
    0: 384x640 (no detections), 12.4ms
    0: 384x640 (no detections), 13.6ms
    0: 384x640 (no detections), 9.7ms
    0: 384x640 (no detections), 16.0ms
    0: 384x640 (no detections), 10.3ms
    0: 384x640 (no detections), 19.7ms
    0: 384x640 (no detections), 11.7ms
    0: 384x640 (no detections), 10.5ms
    0: 384x640 (no detections), 16.0ms
    0: 384x640 (no detections), 16.3ms
    0: 384x640 (no detections), 21.7ms
    0: 384x640 (no detections), 9.5ms
    0: 384x640 (no detections), 9.2ms
    0: 384x640 (no detections), 15.4ms
    0: 384x640 (no detections), 6.5ms
    0: 384x640 (no detections), 11.3ms
    0: 384x640 (no detections), 6.8ms
    0: 384x640 (no detections), 12.2ms
    0: 384x640 (no detections), 16.5ms
    0: 384x640 (no detections), 9.1ms
    0: 384x640 (no detections), 15.2ms
    0: 384x640 (no detections), 11.3ms
    0: 384x640 (no detections), 12.0ms
    0: 384x640 (no detections), 9.7ms
    0: 384x640 (no detections), 18.0ms
    0: 384x640 (no detections), 11.6ms
    0: 384x640 (no detections), 11.8ms
    0: 384x640 (no detections), 9.5ms
    0: 384x640 (no detections), 13.1ms
    0: 384x640 (no detections), 12.1ms
    0: 384x640 (no detections), 16.1ms
    0: 384x640 (no detections), 10.5ms
    0: 384x640 (no detections), 9.5ms
    0: 384x640 (no detections), 9.6ms
    0: 384x640 (no detections), 12.1ms
    0: 384x640 (no detections), 10.7ms
    0: 384x640 (no detections), 8.4ms
    0: 384x640 (no detections), 19.1ms
    0: 384x640 (no detections), 9.0ms
    0: 384x640 (no detections), 15.5ms
    0: 384x640 (no detections), 9.6ms
    0: 384x640 (no detections), 13.0ms
    0: 384x640 (no detections), 9.6ms
    0: 384x640 (no detections), 11.9ms
    0: 384x640 (no detections), 10.3ms
    0: 384x640 (no detections), 9.7ms
    0: 384x640 (no detections), 9.7ms
    0: 384x640 (no detections), 10.5ms
    0: 384x640 (no detections), 22.0ms
    0: 384x640 (no detections), 10.9ms
    0: 384x640 (no detections), 19.7ms
    0: 384x640 (no detections), 8.7ms
    0: 384x640 (no detections), 30.0ms
    0: 384x640 (no detections), 28.1ms
    0: 384x640 (no detections), 34.3ms
    0: 384x640 (no detections), 38.2ms
    0: 384x640 (no detections), 28.7ms
    0: 384x640 (no detections), 26.6ms
    0: 384x640 (no detections), 27.4ms
    0: 384x640 (no detections), 24.6ms
    0: 384x640 (no detections), 30.4ms
    0: 384x640 (no detections), 30.9ms
    0: 384x640 (no detections), 28.4ms
    0: 384x640 (no detections), 17.5ms
    0: 384x640 (no detections), 23.6ms
    0: 384x640 (no detections), 36.7ms
    0: 384x640 (no detections), 31.0ms
    0: 384x640 (no detections), 33.1ms
    0: 384x640 (no detections), 26.7ms
    0: 384x640 (no detections), 20.0ms
    0: 384x640 (no detections), 22.2ms
    0: 384x640 (no detections), 34.6ms
    0: 384x640 (no detections), 28.5ms
    0: 384x640 (no detections), 18.6ms
    0: 384x640 (no detections), 10.8ms
    0: 384x640 (no detections), 12.6ms
    0: 384x640 (no detections), 15.4ms
    0: 384x640 (no detections), 16.7ms
    0: 384x640 (no detections), 12.5ms
    0: 384x640 (no detections), 14.7ms
    0: 384x640 (no detections), 12.8ms
    0: 384x640 (no detections), 12.3ms
    0: 384x640 (no detections), 11.9ms
    0: 384x640 (no detections), 9.9ms
    0: 384x640 (no detections), 31.1ms
    0: 384x640 (no detections), 10.0ms
    0: 384x640 (no detections), 9.1ms
    0: 384x640 (no detections), 17.2ms
    0: 384x640 (no detections), 11.3ms
    0: 384x640 (no detections), 16.2ms
    0: 384x640 (no detections), 10.0ms
    0: 384x640 (no detections), 10.0ms
    0: 384x640 (no detections), 9.6ms
    0: 384x640 (no detections), 12.8ms
    0: 384x640 (no detections), 14.1ms
    0: 384x640 (no detections), 24.1ms
    0: 384x640 (no detections), 11.5ms
    0: 384x640 (no detections), 10.3ms
    0: 384x640 (no detections), 10.6ms
    0: 384x640 (no detections), 18.4ms
    0: 384x640 (no detections), 11.9ms
    0: 384x640 (no detections), 12.2ms
    0: 384x640 (no detections), 10.7ms
    0: 384x640 (no detections), 12.5ms
    0: 384x640 (no detections), 13.8ms
    0: 384x640 (no detections), 16.5ms
    0: 384x640 (no detections), 13.5ms
    0: 384x640 (no detections), 14.1ms
    0: 384x640 (no detections), 7.9ms
    0: 384x640 (no detections), 11.3ms
    0: 384x640 (no detections), 9.4ms
    0: 384x640 (no detections), 10.2ms
    0: 384x640 (no detections), 10.9ms
    0: 384x640 (no detections), 17.3ms
    0: 384x640 (no detections), 9.7ms
    0: 384x640 (no detections), 24.5ms
    0: 384x640 (no detections), 10.6ms
    0: 384x640 (no detections), 11.8ms
    0: 384x640 (no detections), 10.5ms
    0: 384x640 (no detections), 18.0ms
    0: 384x640 (no detections), 12.0ms
    0: 384x640 (no detections), 12.0ms
    0: 384x640 (no detections), 10.7ms
    0: 384x640 (no detections), 10.5ms
    0: 384x640 (no detections), 14.5ms
    0: 384x640 (no detections), 16.9ms
    0: 384x640 (no detections), 13.2ms
    0: 384x640 (no detections), 8.6ms
    0: 384x640 (no detections), 13.5ms
    0: 384x640 (no detections), 16.8ms
    0: 384x640 (no detections), 31.5ms
    0: 384x640 (no detections), 10.4ms
    0: 384x640 (no detections), 10.7ms
    0: 384x640 (no detections), 11.7ms
    0: 384x640 (no detections), 11.7ms
    0: 384x640 (no detections), 11.4ms
    0: 384x640 (no detections), 10.9ms
    0: 384x640 (no detections), 9.9ms
    0: 384x640 (no detections), 11.1ms
    0: 384x640 (no detections), 10.1ms
    0: 384x640 (no detections), 10.8ms
    0: 384x640 (no detections), 7.1ms
    0: 384x640 (no detections), 18.3ms
    0: 384x640 (no detections), 8.4ms
    0: 384x640 (no detections), 22.5ms
    0: 384x640 (no detections), 7.9ms
    0: 384x640 (no detections), 10.4ms
    0: 384x640 (no detections), 10.5ms
    0: 384x640 (no detections), 16.7ms
    0: 384x640 (no detections), 11.4ms
    0: 384x640 (no detections), 11.2ms
    0: 384x640 (no detections), 11.2ms
    0: 384x640 (no detections), 10.8ms
    0: 384x640 (no detections), 13.8ms
    0: 384x640 (no detections), 14.4ms
    0: 384x640 (no detections), 8.5ms
    0: 384x640 (no detections), 10.0ms
    0: 384x640 (no detections), 9.4ms
    0: 384x640 (no detections), 10.0ms
    0: 384x640 (no detections), 10.2ms
    0: 384x640 (no detections), 9.6ms
    0: 384x640 (no detections), 6.8ms
    0: 384x640 (no detections), 8.9ms
    0: 384x640 (no detections), 18.9ms
    0: 384x640 (no detections), 10.3ms
    0: 384x640 (no detections), 8.7ms
    0: 384x640 (no detections), 6.6ms
    0: 384x640 (no detections), 14.2ms
    0: 384x640 (no detections), 13.3ms
    0: 384x640 (no detections), 6.5ms
    0: 384x640 1 Ambulance, 7.0ms
    0: 384x640 1 Ambulance, 9.2ms
    0: 384x640 (no detections), 11.7ms
    0: 384x640 (no detections), 11.6ms
    0: 384x640 (no detections), 15.4ms
    0: 384x640 (no detections), 9.2ms
    0: 384x640 (no detections), 14.0ms
    0: 384x640 (no detections), 10.1ms
    0: 384x640 (no detections), 15.9ms
    0: 384x640 (no detections), 10.4ms
    0: 384x640 (no detections), 16.6ms
    0: 384x640 (no detections), 11.5ms
    0: 384x640 (no detections), 10.6ms
    0: 384x640 (no detections), 17.3ms
    0: 384x640 (no detections), 14.5ms
    0: 384x640 (no detections), 13.0ms
    0: 384x640 (no detections), 14.0ms
    0: 384x640 (no detections), 13.0ms
    0: 384x640 (no detections), 11.0ms
    0: 384x640 (no detections), 10.6ms
    0: 384x640 (no detections), 11.6ms
    0: 384x640 (no detections), 14.0ms
    0: 384x640 (no detections), 16.4ms
    0: 384x640 (no detections), 18.4ms
    0: 384x640 (no detections), 12.4ms
    0: 384x640 (no detections), 13.4ms
    0: 384x640 (no detections), 16.9ms
    0: 384x640 (no detections), 8.8ms
    0: 384x640 (no detections), 6.2ms
    Speed: 4.9ms preprocess, 14.8ms inference, 1.3ms postprocess per image at shape (1, 3, 384, 640)
    Results saved to /content/runs/detect/predict
    Detecção finalizada.
