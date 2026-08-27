# Tarea 1 - Predicción de resultados del fútbol uruguayo

Este directorio contiene tu trabajo para la primera tarea de Aprendizaje Automático. El objetivo es construir modelos que, antes de un partido, predigan una de estas clases:

- `L`: gana el equipo local.
- `V`: gana el equipo visitante.
- `E`: hay empate.

## Cómo abrir el proyecto

1. Abre una terminal.
2. Activa tu entorno virtual. Si está en tu directorio personal, ejecuta:

   ```bash
   source ~/myenv/bin/activate
   ```

3. Ve a esta carpeta:

   ```bash
   cd "/home/francros/Documentos/Aprendizaje Automático/Laboratorio 1/tarea1"
   ```

4. Abre Jupyter Notebook:

   ```bash
   jupyter notebook
   ```

5. En el navegador, abre `tarea1.ipynb`.
6. Ejecuta una celda con `Shift + Enter`. Sigue el notebook de arriba hacia abajo.

## Qué contiene cada elemento

| Elemento | Para qué sirve |
|---|---|
| `tarea1.ipynb` | Aquí escribirás el código, las explicaciones, las tablas, los gráficos y las conclusiones. |
| `resultados/` | Guarda las imágenes finales de gráficas que quieras incluir también en el informe. |
| `informe/` | Guarda el artículo IEEE final y recursos asociados, como tablas o imágenes. |
| `../futbol_uruguayo.csv` | Es el dataset original. No lo modifiques: el notebook debe leerlo directamente. |
| `../Letra Tarea 1.pdf` | Es la letra oficial de la tarea. |

## Recorrido obligatorio del notebook

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

## Reglas críticas

- No uses `gh` ni `ga` como atributos de entrada: son los goles finales del partido y solo sirven para construir la respuesta correcta `winner`.
- Usa para entrenamiento los partidos hasta 2023 inclusive.
- Reserva 2024 y 2025 exclusivamente para la evaluación final.
- Fija las semillas aleatorias, por ejemplo con `RANDOM_STATE = 42`.
- No dependas de un CSV ya procesado: el notebook debe construir todo al ejecutarse desde cero.
- Antes de entregar, usa `Kernel -> Restart Kernel and Run All` para comprobar que el notebook funciona completo.

## Cómo avanzar sin perderte

No intentes hacer toda la tarea de una vez. Completa una sección del notebook, ejecútala y entiende el resultado antes de pasar a la siguiente. Empieza por carga, limpieza y `winner`; después crea atributos simples; recién entonces pasa a los modelos.
