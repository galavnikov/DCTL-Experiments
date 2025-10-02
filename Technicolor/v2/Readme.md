# Technicolorama v2.0

`Technicolorama v2.0` es un script DCTL (DaVinci Resolve Color Transform Language) diseñado para emular los procesos cinematográficos clásicos de Technicolor de 2 y 3 tiras directamente en DaVinci Resolve. Este script ofrece un control detallado sobre la imagen, permitiendo a los coloristas y editores recrear estéticas icónicas con herramientas modernas.

El código fuente está optimizado y depurado siguiendo la documentación oficial de DaVinci Resolve para garantizar la máxima compatibilidad y rendimiento.

## Características Principales

* **Doble Modo de Proceso**: Emula tanto el proceso Technicolor de 3 tiras (RGB) como el de 2 tiras (Rojo y Cian).
* **Controles de Laboratorio**: Ajusta parámetros clave de la imagen como la densidad (brillo), el contraste y la saturación.
* **Tinte General**: Aplica un tinte global a la imagen para corregir o estilizar el balance de color.
* **Aislamiento de Canales**: Permite visualizar cada una de las tiras de color de forma individual (R, G, B o Cian) para un análisis detallado.

## Instalación

1.  Abre DaVinci Resolve.
2.  Ve al menú **Archivo > Configuración del Proyecto**.
3.  En la pestaña **Gestión de color**, desplázate hacia abajo hasta la sección "LUTs".
4.  Haz clic en el botón **"Abrir carpeta de LUTs"**.
5.  Dentro de la carpeta que se ha abierto, localiza y entra en la subcarpeta `DCTL`.
6.  Copia el archivo `Technicolorama v2.0.dctl` en esta carpeta.
7.  Vuelve a DaVinci Resolve y en la misma ventana de configuración haz clic en **"Actualizar listas"**.
8.  El efecto DCTL ya estará disponible en el panel de Nodos, en la sección "Resolve FX > DCTL".

## Flujo de Trabajo Recomendado: Importación de PowerGrades

Para facilitar un flujo de trabajo más intuitivo y comprender cómo funcionaba originalmente el laborioso proceso analógico, se recomienda importar los PowerGrades correspondientes a los procesos de 2 y 3 tiras.

Estos PowerGrades contienen una estructura de nodos preconfigurada que simula la separación y recombinación de las tiras de color, tal como se hacía en el laboratorio. Al utilizar estos PowerGrades:

* **Simplificas el Proceso**: La estructura de nodos ya está creada, permitiéndote aplicar el look de forma rápida y consistente.
* **Aprendizaje Visual**: Podrás visualizar cómo se descompone la señal de color, se procesa cada "tira" por separado (donde se aplicaría este DCTL) y se vuelve a combinar para crear la imagen final. Esto ofrece una valiosa perspectiva sobre la complejidad del Technicolor original.

**Instrucciones de Importación:**
1.  Ve a la Galería de DaVinci Resolve.
2.  Haz clic derecho en el área de "Stills" y selecciona "Importar".
3.  Busca y selecciona los archivos `.drx` de los PowerGrades y haz clic en "Importar".
4.  Una vez importados, podrás arrastrarlos a un nodo en tu corrección de color.

## Parámetros del Script

El script `Technicolorama v2.0` expone los siguientes controles en la interfaz de DaVinci Resolve:

* **Proceso Technicolor**: Un menú desplegable para elegir entre los dos modos de emulación.
    * `3 Strips RGB`: Simula el proceso clásico de tres tiras, utilizando los canales Rojo, Verde y Azul.
    * `2 strips R and Cian`: Simula el proceso más antiguo de dos tiras, que se basa en un componente Rojo y uno Cian (creado a partir de la media de Verde y Azul).
* **Show R / Show G / Show B / Show Cian**: Casillas de verificación para aislar y visualizar los canales de color individuales. Las opciones disponibles cambian según el modo seleccionado.
* **Density**: Un deslizador que controla el brillo general de la imagen, similar a la densidad de la película.
* **Contrast**: Ajusta el contraste de la imagen, modificando la separación entre las luces y las sombras.
* **Saturation**: Controla la intensidad global del color en la imagen.
* **Tint**: Aplica un desplazamiento de matiz a toda la imagen, permitiendo corregir dominantes de color o añadir un estilo creativo.

## Funcionamiento Interno

El script sigue una secuencia de pasos lógicos para transformar la imagen de entrada:

1.  **Selección del Proceso**: Se elige entre el modelo de 3 o 2 tiras. En el caso de 2 tiras, los canales verde y azul se combinan para crear el componente cian.
2.  **Ajustes de Laboratorio**: Se aplican secuencialmente los ajustes de contraste, saturación y densidad (brillo).
3.  **Tinte General**: Si se ha modificado el parámetro "Tint", la imagen se convierte al espacio de color HSV para rotar el matiz y luego se revierte a RGB.
4.  **Aislamiento de Canales**: Finalmente, si alguna de las casillas "Show" está desactivada, los canales correspondientes se anulan (se ponen a cero) para mostrar únicamente los seleccionados.
5.  **Salida**: La imagen procesada se devuelve al nodo para su visualización.

