# Tarea 1 - Predicción de resultados del fútbol uruguayo

Este directorio contiene el trabajo de la primera tarea de Aprendizaje Automático. El objetivo es construir y comparar modelos que, antes de un partido, predigan uno de los siguientes resultados:

- `L`: gana el equipo local.
- `V`: gana el equipo visitante.
- `E`: el partido termina en empate.

## Requisitos

Para ejecutar el proyecto se necesita Python 3, Jupyter Notebook y las bibliotecas utilizadas dentro de `tarea1.ipynb`. Se recomienda trabajar en un entorno virtual para mantener las dependencias aisladas.

## Cómo ejecutar el proyecto

1. Clonar el repositorio y entrar en esta carpeta:

   ```bash
   git clone https://github.com/AlonsoNahuel/Aprendizaje_Automatico.git
   cd Aprendizaje_Automatico/tarea1
   ```

2. Activar el entorno virtual correspondiente, si se utiliza uno.
3. Iniciar Jupyter Notebook:

   ```bash
   jupyter notebook
   ```

4. Abrir `tarea1.ipynb` y ejecutar las celdas en orden, de arriba hacia abajo.

> Las rutas son relativas al repositorio. No es necesario guardarlo en una ubicación específica de la computadora.

## Estructura relevante

| Ruta | Descripción |
|---|---|
| `tarea1/tarea1.ipynb` | Notebook principal con el código, las explicaciones, las tablas, los gráficos y las conclusiones. |
| `futbol_uruguayo/futbol_uruguayo.csv` | Dataset original utilizado por el notebook. No debe modificarse. |
| `Tarea_1.pdf` | Letra oficial de la tarea. |

Visto desde la carpeta `tarea1`, la ruta relativa del dataset es `../futbol_uruguayo/futbol_uruguayo.csv`.

## Etapas del trabajo

1. Cargar e inspeccionar los partidos.
2. Limpiar datos y crear la clase `winner`.
3. Crear atributos que estén disponibles antes del partido.
4. Separar temporalmente entrenamiento y evaluación.
5. Implementar el clasificador base de los últimos diez años.
6. Implementar el árbol de decisión propio.
7. Implementar Naive Bayes propio.
8. Entrenar Random Forest y Naive Bayes de scikit-learn.
9. Ajustar hiperparámetros con validación temporal.
10. Evaluar, comparar, graficar y analizar los resultados.

## Consideraciones importantes

- `gh` y `ga` no deben usarse como atributos de entrada: son los goles finales del partido y solo sirven para construir la variable objetivo `winner`.
- Los partidos hasta 2023 inclusive se utilizan para entrenamiento.
- Los datos de 2024 y 2025 se reservan exclusivamente para la evaluación final.
- Las semillas aleatorias deben fijarse para obtener resultados reproducibles; por ejemplo, `RANDOM_STATE = 42`.
- El notebook debe procesar el dataset original desde cero y no depender de un CSV previamente transformado.
- Antes de entregar, conviene reiniciar el kernel y ejecutar todas las celdas para comprobar que el notebook funciona completo.

## Forma de trabajo recomendada

El notebook puede completarse por etapas: primero la carga, la limpieza y la creación de `winner`; luego la construcción de atributos; y finalmente el entrenamiento y la evaluación de los modelos. Ejecutar y revisar cada sección antes de continuar facilita la detección de errores.
