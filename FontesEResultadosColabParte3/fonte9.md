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

    0: 384x640 (no detections), 13.7ms
    0: 384x640 (no detections), 10.5ms
    0: 384x640 (no detections), 10.2ms
    0: 384x640 (no detections), 11.3ms
    0: 384x640 (no detections), 14.8ms
    0: 384x640 (no detections), 10.0ms
    0: 384x640 (no detections), 38.6ms
    0: 384x640 (no detections), 28.5ms
    0: 384x640 (no detections), 24.8ms
    0: 384x640 (no detections), 16.8ms
    0: 384x640 (no detections), 69.8ms
    0: 384x640 (no detections), 43.8ms
    0: 384x640 (no detections), 41.8ms
    0: 384x640 (no detections), 11.2ms
    0: 384x640 (no detections), 14.6ms
    0: 384x640 (no detections), 65.5ms
    0: 384x640 (no detections), 70.8ms
    0: 384x640 (no detections), 52.9ms
    0: 384x640 (no detections), 32.4ms
    0: 384x640 (no detections), 10.0ms
    0: 384x640 (no detections), 14.8ms
    0: 384x640 (no detections), 15.5ms
    0: 384x640 (no detections), 10.7ms
    0: 384x640 (no detections), 10.0ms
    0: 384x640 1 Ambulance, 10.7ms
    0: 384x640 (no detections), 13.5ms
    0: 384x640 (no detections), 11.8ms
    0: 384x640 (no detections), 19.9ms
    0: 384x640 (no detections), 9.9ms
    0: 384x640 (no detections), 13.5ms
    0: 384x640 (no detections), 20.9ms
    0: 384x640 (no detections), 14.3ms
    0: 384x640 (no detections), 9.7ms
    0: 384x640 (no detections), 53.8ms
    0: 384x640 (no detections), 55.8ms
    0: 384x640 (no detections), 21.9ms
    0: 384x640 (no detections), 46.6ms
    0: 384x640 (no detections), 14.4ms
    0: 384x640 (no detections), 9.5ms
    0: 384x640 (no detections), 20.3ms
    0: 384x640 (no detections), 27.0ms
    0: 384x640 (no detections), 18.5ms
    0: 384x640 (no detections), 32.7ms
    0: 384x640 (no detections), 18.6ms
    0: 384x640 (no detections), 35.1ms
    0: 384x640 (no detections), 34.3ms
    0: 384x640 (no detections), 65.6ms
    0: 384x640 1 Ambulance, 39.4ms
    0: 384x640 (no detections), 46.6ms
    0: 384x640 (no detections), 13.3ms
    0: 384x640 (no detections), 30.4ms
    0: 384x640 (no detections), 27.4ms
    0: 384x640 (no detections), 34.6ms
    0: 384x640 (no detections), 27.5ms
    0: 384x640 (no detections), 25.4ms
    0: 384x640 (no detections), 21.8ms
    0: 384x640 (no detections), 23.0ms
    0: 384x640 (no detections), 29.5ms
    0: 384x640 (no detections), 26.2ms
    0: 384x640 (no detections), 25.1ms
    0: 384x640 (no detections), 12.1ms
    0: 384x640 (no detections), 10.6ms
    0: 384x640 (no detections), 29.6ms
    0: 384x640 (no detections), 18.0ms
    0: 384x640 (no detections), 21.4ms
    WARNING ⚠️ Waiting for stream 0
    WARNING ⚠️ Waiting for stream 0
    WARNING ⚠️ Waiting for stream 0
    WARNING ⚠️ Waiting for stream 0
    WARNING ⚠️ Waiting for stream 0
    WARNING ⚠️ Waiting for stream 0
    WARNING ⚠️ Waiting for stream 0
    WARNING ⚠️ Waiting for stream 0
    WARNING ⚠️ Waiting for stream 0
    WARNING ⚠️ Waiting for stream 0
    WARNING ⚠️ Waiting for stream 0
    0: 384x640 (no detections), 22.6ms
    0: 384x640 (no detections), 10.4ms
    0: 384x640 (no detections), 10.4ms
    0: 384x640 (no detections), 17.9ms
    0: 384x640 (no detections), 11.8ms
    0: 384x640 (no detections), 11.8ms
    0: 384x640 (no detections), 13.1ms
    0: 384x640 (no detections), 11.7ms
    0: 384x640 (no detections), 15.0ms
    0: 384x640 (no detections), 21.5ms
    0: 384x640 (no detections), 17.6ms
    0: 384x640 (no detections), 11.1ms
    0: 384x640 (no detections), 21.0ms
    0: 384x640 (no detections), 13.0ms
    0: 384x640 (no detections), 14.9ms
    0: 384x640 (no detections), 13.5ms
    0: 384x640 (no detections), 11.7ms
    0: 384x640 (no detections), 10.1ms
    0: 384x640 (no detections), 13.3ms
    0: 384x640 (no detections), 9.9ms
    0: 384x640 (no detections), 15.0ms
    0: 384x640 (no detections), 13.7ms
    0: 384x640 (no detections), 12.2ms
    0: 384x640 (no detections), 19.3ms
    0: 384x640 (no detections), 16.8ms
    0: 384x640 (no detections), 11.3ms
    0: 384x640 (no detections), 10.2ms
    0: 384x640 (no detections), 16.9ms
    0: 384x640 (no detections), 11.3ms
    0: 384x640 (no detections), 18.5ms
    0: 384x640 (no detections), 19.3ms
    WARNING ⚠️ Waiting for stream 0
    0: 384x640 (no detections), 16.5ms
    0: 384x640 (no detections), 16.8ms
    0: 384x640 (no detections), 9.8ms
    0: 384x640 (no detections), 11.1ms
    0: 384x640 (no detections), 13.6ms
    0: 384x640 (no detections), 10.0ms
    0: 384x640 (no detections), 11.0ms
    0: 384x640 (no detections), 10.7ms
    0: 384x640 (no detections), 12.4ms
    0: 384x640 (no detections), 15.5ms
    0: 384x640 (no detections), 31.1ms
    0: 384x640 (no detections), 19.2ms
    0: 384x640 (no detections), 15.3ms
    0: 384x640 (no detections), 10.8ms
    0: 384x640 (no detections), 10.1ms
    0: 384x640 (no detections), 10.5ms
    0: 384x640 (no detections), 10.2ms
    0: 384x640 (no detections), 12.2ms
    0: 384x640 (no detections), 28.4ms
    0: 384x640 (no detections), 34.6ms
    0: 384x640 (no detections), 56.4ms
    0: 384x640 (no detections), 73.2ms
    0: 384x640 (no detections), 14.0ms
    0: 384x640 (no detections), 11.8ms
    0: 384x640 (no detections), 12.5ms
    0: 384x640 (no detections), 11.7ms
    0: 384x640 (no detections), 19.8ms
    0: 384x640 (no detections), 14.3ms
    0: 384x640 (no detections), 9.7ms
    0: 384x640 (no detections), 10.0ms
    0: 384x640 (no detections), 11.0ms
    0: 384x640 (no detections), 10.4ms
    0: 384x640 (no detections), 10.1ms
    0: 384x640 (no detections), 11.9ms
    0: 384x640 (no detections), 12.1ms
    0: 384x640 (no detections), 10.6ms
    0: 384x640 (no detections), 24.2ms
    0: 384x640 (no detections), 10.1ms
    0: 384x640 (no detections), 21.7ms
    0: 384x640 (no detections), 15.0ms
    0: 384x640 (no detections), 10.4ms
    0: 384x640 (no detections), 26.4ms
    0: 384x640 (no detections), 21.6ms
    0: 384x640 (no detections), 41.0ms
    0: 384x640 (no detections), 19.3ms
    0: 384x640 (no detections), 11.8ms
    0: 384x640 (no detections), 10.3ms
    0: 384x640 (no detections), 18.9ms
    WARNING ⚠️ Waiting for stream 0
    WARNING ⚠️ Waiting for stream 0
    WARNING ⚠️ Waiting for stream 0
    WARNING ⚠️ Waiting for stream 0
    0: 384x640 (no detections), 14.3ms
    0: 384x640 (no detections), 10.3ms
    0: 384x640 (no detections), 18.0ms
    0: 384x640 (no detections), 10.1ms
    0: 384x640 (no detections), 20.3ms
    0: 384x640 (no detections), 36.8ms
    0: 384x640 (no detections), 24.2ms
    0: 384x640 (no detections), 18.1ms
    0: 384x640 (no detections), 12.0ms
    0: 384x640 (no detections), 17.6ms
    0: 384x640 (no detections), 11.9ms
    0: 384x640 (no detections), 20.8ms
    0: 384x640 (no detections), 10.0ms
    0: 384x640 (no detections), 9.9ms
    0: 384x640 (no detections), 10.2ms
    0: 384x640 (no detections), 15.0ms
    0: 384x640 (no detections), 9.9ms
    0: 384x640 (no detections), 11.3ms
    0: 384x640 (no detections), 19.6ms
    0: 384x640 (no detections), 21.8ms
    0: 384x640 (no detections), 9.9ms
    0: 384x640 (no detections), 12.9ms
    0: 384x640 (no detections), 16.8ms
    0: 384x640 (no detections), 12.5ms
    0: 384x640 (no detections), 18.5ms
    0: 384x640 (no detections), 10.0ms
    0: 384x640 (no detections), 10.3ms
    0: 384x640 (no detections), 20.0ms
    WARNING ⚠️ Waiting for stream 0
    0: 384x640 (no detections), 14.2ms
    0: 384x640 (no detections), 13.2ms
    0: 384x640 (no detections), 12.7ms
    0: 384x640 (no detections), 15.4ms
    0: 384x640 (no detections), 23.3ms
    0: 384x640 (no detections), 20.3ms
    0: 384x640 (no detections), 17.3ms
    0: 384x640 (no detections), 25.3ms
    0: 384x640 (no detections), 12.3ms
    0: 384x640 (no detections), 11.6ms
    0: 384x640 (no detections), 20.9ms
    0: 384x640 (no detections), 25.0ms
    0: 384x640 (no detections), 19.3ms
    0: 384x640 (no detections), 57.3ms
    0: 384x640 (no detections), 21.7ms
    0: 384x640 (no detections), 48.7ms
    0: 384x640 (no detections), 17.0ms
    0: 384x640 (no detections), 18.1ms
    WARNING ⚠️ Waiting for stream 0
    0: 384x640 (no detections), 22.3ms
    0: 384x640 (no detections), 29.0ms
    0: 384x640 (no detections), 28.5ms
    0: 384x640 (no detections), 27.1ms
    0: 384x640 (no detections), 23.9ms
    0: 384x640 (no detections), 19.4ms
    WARNING ⚠️ Waiting for stream 0
    0: 384x640 (no detections), 42.9ms
    0: 384x640 (no detections), 22.6ms
    0: 384x640 (no detections), 22.3ms
    0: 384x640 (no detections), 43.9ms
    0: 384x640 (no detections), 28.0ms
    0: 384x640 (no detections), 25.7ms
    0: 384x640 (no detections), 19.3ms
    0: 384x640 (no detections), 18.4ms
    0: 384x640 (no detections), 27.9ms
    0: 384x640 (no detections), 24.0ms
    0: 384x640 (no detections), 28.2ms
    0: 384x640 (no detections), 15.4ms
    0: 384x640 (no detections), 15.9ms
    0: 384x640 (no detections), 13.8ms
    0: 384x640 (no detections), 21.0ms
    0: 384x640 (no detections), 11.0ms
    0: 384x640 (no detections), 10.7ms
    0: 384x640 (no detections), 10.6ms
    0: 384x640 (no detections), 10.6ms
    0: 384x640 (no detections), 10.8ms
    0: 384x640 (no detections), 13.1ms
    0: 384x640 (no detections), 10.3ms
    0: 384x640 (no detections), 14.3ms
    0: 384x640 (no detections), 23.2ms
    0: 384x640 (no detections), 24.9ms
    0: 384x640 (no detections), 10.8ms
    0: 384x640 (no detections), 9.7ms
    0: 384x640 (no detections), 20.7ms
    0: 384x640 (no detections), 11.5ms
    0: 384x640 (no detections), 12.1ms
    0: 384x640 (no detections), 15.6ms
    0: 384x640 (no detections), 14.6ms
    0: 384x640 (no detections), 24.7ms
    0: 384x640 (no detections), 31.3ms
    0: 384x640 (no detections), 12.8ms
    0: 384x640 (no detections), 15.1ms
    0: 384x640 (no detections), 11.9ms
    0: 384x640 (no detections), 10.5ms
    0: 384x640 (no detections), 13.0ms
    0: 384x640 (no detections), 11.5ms
    0: 384x640 (no detections), 23.9ms
    0: 384x640 (no detections), 15.1ms
    0: 384x640 (no detections), 12.5ms
    0: 384x640 (no detections), 19.4ms
    0: 384x640 (no detections), 16.8ms
    0: 384x640 (no detections), 11.1ms
    0: 384x640 (no detections), 11.7ms
    0: 384x640 (no detections), 12.9ms
    0: 384x640 (no detections), 14.9ms
    0: 384x640 (no detections), 19.3ms
    0: 384x640 (no detections), 12.4ms
    0: 384x640 (no detections), 18.4ms
    0: 384x640 (no detections), 17.5ms
    0: 384x640 (no detections), 9.7ms
    0: 384x640 (no detections), 29.6ms
    0: 384x640 (no detections), 11.4ms
    0: 384x640 (no detections), 9.6ms
    0: 384x640 (no detections), 9.8ms
    0: 384x640 (no detections), 39.6ms
    0: 384x640 (no detections), 15.9ms
    0: 384x640 (no detections), 10.8ms
    0: 384x640 (no detections), 10.6ms
    0: 384x640 (no detections), 14.2ms
    0: 384x640 (no detections), 15.0ms
    0: 384x640 (no detections), 21.0ms
    WARNING ⚠️ Waiting for stream 0
    WARNING ⚠️ Waiting for stream 0
    WARNING ⚠️ Waiting for stream 0
    WARNING ⚠️ Waiting for stream 0
    WARNING ⚠️ Waiting for stream 0
    WARNING ⚠️ Waiting for stream 0
    WARNING ⚠️ Waiting for stream 0
    0: 384x640 (no detections), 36.5ms
    0: 384x640 (no detections), 13.4ms
    0: 384x640 (no detections), 10.7ms
    0: 384x640 (no detections), 18.6ms
    0: 384x640 (no detections), 32.8ms
    0: 384x640 (no detections), 15.4ms
    0: 384x640 (no detections), 17.1ms
    0: 384x640 (no detections), 19.9ms
    0: 384x640 (no detections), 25.1ms
    0: 384x640 (no detections), 9.9ms
    0: 384x640 (no detections), 10.3ms
    0: 384x640 (no detections), 10.1ms
    0: 384x640 (no detections), 10.7ms
    0: 384x640 (no detections), 14.8ms
    0: 384x640 (no detections), 10.4ms
    0: 384x640 (no detections), 19.1ms
    0: 384x640 (no detections), 10.7ms
    0: 384x640 (no detections), 22.0ms
    WARNING ⚠️ Waiting for stream 0
    WARNING ⚠️ Waiting for stream 0
    WARNING ⚠️ Waiting for stream 0
    WARNING ⚠️ Waiting for stream 0
    WARNING ⚠️ Waiting for stream 0
    WARNING ⚠️ Waiting for stream 0
    WARNING ⚠️ Waiting for stream 0
    WARNING ⚠️ Waiting for stream 0
    WARNING ⚠️ Waiting for stream 0
    0: 384x640 (no detections), 19.2ms
    0: 384x640 (no detections), 17.0ms
    0: 384x640 (no detections), 9.4ms
    0: 384x640 (no detections), 22.8ms
    WARNING ⚠️ Waiting for stream 0
    0: 384x640 (no detections), 10.4ms
    0: 384x640 (no detections), 10.3ms
    0: 384x640 (no detections), 15.3ms
    0: 384x640 (no detections), 9.8ms
    0: 384x640 (no detections), 15.1ms
    0: 384x640 (no detections), 24.7ms
    0: 384x640 (no detections), 22.1ms
    0: 384x640 (no detections), 18.2ms
    0: 384x640 (no detections), 17.1ms
    0: 384x640 (no detections), 23.1ms
    0: 384x640 (no detections), 10.1ms
    0: 384x640 (no detections), 17.8ms
    0: 384x640 (no detections), 18.0ms
    WARNING ⚠️ Waiting for stream 0
    WARNING ⚠️ Waiting for stream 0
    WARNING ⚠️ Waiting for stream 0
    WARNING ⚠️ Waiting for stream 0
    WARNING ⚠️ Waiting for stream 0
    WARNING ⚠️ Waiting for stream 0
    WARNING ⚠️ Waiting for stream 0
    WARNING ⚠️ Waiting for stream 0
    WARNING ⚠️ Waiting for stream 0
    WARNING ⚠️ Waiting for stream 0
    WARNING ⚠️ Waiting for stream 0
    WARNING ⚠️ Waiting for stream 0
    WARNING ⚠️ Waiting for stream 0
    WARNING ⚠️ Waiting for stream 0
    WARNING ⚠️ Waiting for stream 0
    0: 384x640 (no detections), 55.9ms
    0: 384x640 (no detections), 10.3ms
    0: 384x640 (no detections), 19.9ms
    0: 384x640 (no detections), 20.5ms
    0: 384x640 (no detections), 18.9ms
    0: 384x640 (no detections), 19.6ms
    0: 384x640 (no detections), 15.2ms
    0: 384x640 (no detections), 10.0ms
    0: 384x640 (no detections), 9.7ms
    0: 384x640 (no detections), 48.3ms
    0: 384x640 (no detections), 19.6ms
    0: 384x640 (no detections), 10.4ms
    0: 384x640 (no detections), 19.0ms
    0: 384x640 (no detections), 18.8ms
    0: 384x640 (no detections), 14.0ms
    0: 384x640 (no detections), 10.0ms
    0: 384x640 (no detections), 12.9ms
    0: 384x640 (no detections), 9.9ms
    0: 384x640 (no detections), 15.3ms
    0: 384x640 (no detections), 9.9ms
    0: 384x640 (no detections), 13.7ms
    0: 384x640 (no detections), 11.5ms
    0: 384x640 (no detections), 14.2ms
    0: 384x640 (no detections), 17.0ms
    0: 384x640 (no detections), 11.3ms
    0: 384x640 (no detections), 11.1ms
    0: 384x640 (no detections), 14.9ms
    0: 384x640 (no detections), 17.7ms
    0: 384x640 (no detections), 11.9ms
    0: 384x640 (no detections), 10.9ms
    0: 384x640 (no detections), 14.0ms
    0: 384x640 (no detections), 28.1ms
    0: 384x640 (no detections), 27.3ms
    0: 384x640 (no detections), 61.6ms
    0: 384x640 (no detections), 26.5ms
    0: 384x640 (no detections), 22.0ms
    0: 384x640 (no detections), 9.2ms
    0: 384x640 (no detections), 22.5ms
    0: 384x640 (no detections), 17.2ms
    0: 384x640 (no detections), 43.9ms
    0: 384x640 (no detections), 13.1ms
    0: 384x640 (no detections), 8.5ms
    Speed: 6.2ms preprocess, 19.1ms inference, 1.7ms postprocess per image at shape (1, 3, 384, 640)
    Results saved to /content/runs/detect/predict-2
    Detecção finalizada.
