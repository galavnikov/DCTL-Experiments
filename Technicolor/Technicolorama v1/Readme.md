# Technicolorama v1.0 - Emulador de Proceso Technicolor (2 y 3 Strips)

Revive la estética de la época dorada del cine con este DCTL (DaVinci Color Transform Language) para DaVinci Resolve. Emula los icónicos procesos Technicolor de 2 y 3 tiras, ofreciendo un control detallado sobre la intensidad de cada color y el característico "sangrado de color" (color bleeding) para conseguir un look de película vintage auténtico.

## Descripción Detallada y Filosofía
Technicolorama es un DCTL diseñado para simular los procesos de filmación e impresión Technicolor. A diferencia de un LUT estático, proporciona parámetros dinámicos para personalizar completamente el efecto.

Permite a coloristas y editores recrear con precisión el mundo vibrante y saturado del cine clásico. Es ideal para dar un carácter único a vídeos musicales, cortometrajes o cualquier pieza que busque una estética nostálgica y rica en color.

La herramienta se basa en los dos procesos Technicolor más famosos:

* Proceso de 2 Tiras (2-Strip): Una versión anterior que creaba una imagen distintiva a partir de componentes rojo y cian.
  
* Proceso de 3 Tiras (3-Strip): Que registraba la luz en tres negativos distintos (rojo, verde y azul) para luego combinarlos.

## Parámetros y Controles
Este DCTL ofrece los siguientes controles en la interfaz de DaVinci Resolve:

* Proceso Technicolor (Technicolor Process): Un menú desplegable para elegir entre los dos modos de simulación.

  * 3 Tiras (RGB): Emula el proceso Technicolor más avanzado, trabajando con los canales Rojo, Verde y Azul.  
  * 2 Tiras (Rojo y Cian): Emula el proceso más antiguo, generando una imagen basada en un componente rojo y uno cian.

* Intensidad de Tira Roja (Red Strip Intensity): Controla la fuerza del canal rojo en ambos modos.

* Intensidad de Tira Verde/Cian (Green/Cyan Strip Intensity):

  * En modo 3 tiras, ajusta la intensidad del canal verde.
  * En modo 2 tiras, ajusta la intensidad del componente cian, que se genera a partir de la información original del canal verde y azul.

* Intensidad de Tira Azul (Blue Strip Intensity): En modo 3 tiras, ajusta la intensidad del canal azul. Este deslizador se ignora y no tiene efecto en el modo 2 tiras.

* Sangrado de Color (Color Bleeding): Este deslizador simula la imperfección del proceso de tintado, donde los colores "sangran" o se mezclan entre sí. Mezcla cada canal de color con un promedio de los otros dos. Este efecto solo está activo en el modo 3 tiras.

* Contraste de Impresión (Print Contrast): Aplica una curva de contraste final a toda la imagen para emular la apariencia densa de una impresión física de película. Este ajuste se aplica a la... (El texto original se corta aquí).
