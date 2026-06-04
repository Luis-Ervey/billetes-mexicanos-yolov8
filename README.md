# Reconocimiento y Conteo de Billetes Mexicanos mediante Fine-Tuning de YOLOv8

Trabajo Terminal I — **TT2026-2_IA16**
Ingeniería en Inteligencia Artificial · UPIIT-IPN, Campus Tlaxcala

Sistema de detección y conteo de billetes mexicanos (denominaciones $20, $50,
$100, $200, $500 y $1000) mediante *fine-tuning* de YOLOv8, enfocado a la
asistencia de personas con discapacidad visual.

---

## Objetivo

Detectar y contar billetes mexicanos vigentes en una imagen, reportando las
denominaciones presentes y el monto total. El modelo se obtiene aplicando
*fine-tuning* con descongelamiento gradual sobre YOLOv8s pre-entrenado en COCO.

## Estructura del repositorio

```
.
├── README.md                      Este archivo
├── requirements.txt               Dependencias
├── data.yaml                      Configuración del dataset (clases y rutas)
├── notebooks/
│   └── entrenamiento_yolov8.ipynb Notebook de entrenamiento y evaluación
└── .gitignore
```

## Dataset

Dataset propio de billetes mexicanos vigentes, construido y etiquetado en
formato YOLO. Incluye variaciones controladas de iluminación, fondo, ángulo,
estado de conservación y orientación, así como escenas con múltiples billetes.

> Las imágenes del dataset no se incluyen en este repositorio por su tamaño.

## Clases

| ID | Clase          |
|----|----------------|
| 0  | billete_20     |
| 1  | billete_50     |
| 2  | billete_100    |
| 3  | billete_200    |
| 4  | billete_500    |
| 5  | billete_1000   |

## Reproducción

1. Instalar dependencias: `pip install -r requirements.txt`
2. Colocar el dataset exportado de Roboflow (formato YOLOv8) y ajustar las rutas
   en `data.yaml`.
3. Ejecutar el notebook `notebooks/entrenamiento_yolov8.ipynb` (en Kaggle o
   Google Colab con GPU). La semilla aleatoria está fijada para reproducibilidad.

## Entorno

- Python 3.10+
- Ultralytics YOLOv8
- Entrenamiento en cuaderno en la nube con GPU (Kaggle / Google Colab, T4 / P100)

## Estado del proyecto

En desarrollo (Trabajo Terminal I). Dataset construido y etiquetado; pipeline de
entrenamiento implementado. La ejecución de las corridas y la evaluación
(métricas y matriz de confusión) están en proceso.

## Autor

Luis Ervey Guzmán Hernández — UPIIT-IPN
Asesor: M.C. Gerardo Texis Texis
