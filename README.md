# yolo-api--ver2-
[Версия 2] Переводит метки на изображении, через кастомную отрисовку

Работает порог уверенности, переводит названия в таблице

Сжимает фото для ускорения обработки и предотвращения выхода за лимит 512 мб на Render.com

В файле "model_config.json" должно быть:

{
  "model_name": "yolov8n.pt",
  "translate_name": "coco.csv",
  "font_file": "Geoform.ttf"
}

или

{
  "model_name": "yolov8n-oiv7.pt",
  "translate_name": "OpenImagesV7.csv",
  "font_file": "Geoform.ttf"
}

или

{
  "model_name": "yolo10n.pt",
  "translate_name": "coco.csv",
  "font_file": "Geoform.ttf"
}

или

{
  "model_name": "yolo11n.pt",
  "translate_name": "coco.csv",
  "font_file": "Geoform.ttf"
}

или для другой по аналогии.

Важно: Шрифт нужен с поддержкой кирилицы.

На Render в "Start Command" нужно указать: 
uvicorn main:app --host 0.0.0.0 --port $PORT
