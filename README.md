# RedesNeuronales

Aplicación web con Streamlit para reconocer dígitos escritos a mano (0-9) usando un modelo de clasificación entrenado con MNIST.

## Requisitos

- Python 3.10+ (recomendado)
- Dependencias de `requirements.txt`

## Instalación

1. Clona este repositorio.
2. Instala dependencias:

```bash
pip install -r requirements.txt
```

## Ejecución

Inicia la aplicación con:

```bash
streamlit run app.py
```

Luego abre la URL local que muestra Streamlit en tu navegador.

## Uso

1. Sube un archivo de modelo Keras en formato `.h5` (por ejemplo, `modelo_mnist.h5`).
2. Dibuja un dígito en el canvas.
3. Pulsa **Predecir** para obtener:
   - Dígito predicho.
   - Confianza del modelo.

## Estructura del proyecto

- `/home/runner/work/RedesNeuronales/RedesNeuronales/app.py`: interfaz Streamlit y lógica de inferencia.
- `/home/runner/work/RedesNeuronales/RedesNeuronales/requirements.txt`: dependencias del proyecto.

## Notas

- La app requiere cargar el modelo en cada sesión para habilitar la predicción.
- Internamente la imagen se convierte a escala de grises, se redimensiona a `28x28`, se normaliza y se transforma al formato de entrada esperado por el modelo.
