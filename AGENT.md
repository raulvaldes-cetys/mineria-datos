Paso 2: Preparar Visual Studio Code
Asumiendo que ya tienen VS Code instalado para sus otras materias, solo necesitamos prepararlo:

Abre VS Code.
Ve a la sección de Extensiones (Ctrl+Shift+X o Cmd+Shift+X).
Busca e instala las siguientes dos extensiones oficiales de Microsoft:
Python
Jupyter


Paso 3: Crear el Entorno Virtual y Descargar Dependencias
Vamos a crear una "caja de arena" aislada específicamente para esta materia.

Abre tu terminal y ejecuta el siguiente comando para crear un entorno llamado mineria_datos usando Python 3.10:
conda create --name mineria_datos python=3.10 -y
Activa el entorno recién creado:
conda activate mineria_datos
(Deberías ver (mineria_datos) al inicio de la línea de tu terminal).

Instala las librerías fundamentales que usaremos la próxima semana:
conda install numpy pandas jupyter -y


Paso 4: "Prueba de Vida" (Evidencia a entregar)
Para demostrar que su entorno funciona correctamente, harán lo siguiente:

Creen una carpeta para la materia y ábranla en VS Code.
Creen un archivo nuevo llamado test_entorno.ipynb. Al poner la extensión .ipynb, VS Code lo reconocerá automáticamente como un Jupyter Notebook.
En la esquina superior derecha del notebook en VS Code, hagan clic en el botón de "Select Kernel" (o "Seleccionar núcleo"). Elijan Jupyter Kernel y busquen el entorno que acabamos de crear: mineria_datos.
En la primera celda de código, escriban y ejecuten (Shift + Enter) lo siguiente:
import pandas as pd
import numpy as np
 
 
datos = pd.Series([10, 20, 30, 40, 50])
print("¡Entorno configurado con éxito!")
print(datos.describe())
