# ine_detection_yolov5
Modelo entrenado encima de Ultralytics' YOLOV5 para detectar información en las credenciales de elector del INE.

Este modelo es más una prueba que un producto completo: se parte de la versión de YoloV4 en PyTorch construida por Ultralytics y se re-entrena con un dataset de fotografías de credenciales de elector (las cuales no se incluyen por razones de privacidad). 

El resultado, en formato .pt, es funcional y es capáz de detectar las áreas en donde se encuentran la información necesaria (cinco clases: address, clave_de_elector, curp, dob, name); el problema son los pasos anteriores/siguientes, como limpiar la imágen con OpenCV y/o utilizar OCR para entender que es lo que indica (y hacer validaciones, como contrastar con un diccionario de códigos postales o información de Open Street).
