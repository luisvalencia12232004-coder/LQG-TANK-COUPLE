
 Implementación de un Controlador LQG para Tanques Acoplados: Enfoque bajo el Estándar IEC 61131-3
 Autores y Afiliaciones

Luis Enrique Valencia-Salazar** 

Departamento de Ingeniería Electrónica, Universidad Nacional de San Agustín (UNSA), Arequipa, Perú 

Email: (Agrega tu correo aquí)

Alejandro Montana-Bejarano** 

Departamento de Ingeniería Electrónica, Universidad Nacional de San Agustín (UNSA), Arequipa, Perú 

Email: (Agrega el correo de Alejandro aquí)

Descripción

Este repositorio contiene los recursos, scripts y modelos necesarios para reproducir los resultados del artículo: **"Implementación de un Controlador LQG para Tanques Acoplados: Enfoque bajo el Estándar IEC 61131-3"**.

El proyecto presenta el diseño y la validación de una estrategia de control óptimo **Lineal-Cuadrático-Gaussiano (LQG)** aplicada a un sistema de tanques acoplados (CTS). El sistema utiliza un **Filtro de Kalman** para la estimación de estados en presencia de ruido y un regulador **LQR** para la optimización energética.

 Características Principales:

Gemelo Digital:** Desarrollo de un modelo digital en **Factory I/O** para tanques acoplados en cascada, basado en una planta real de Quanser.


Estándar Industrial:** Implementación del algoritmo en un PLC utilizando lenguaje de **Texto Estructurado (SCL)** bajo el estándar **IEC 61131-3**.


Control Avanzado:** Comparativa de desempeño entre el controlador LQG y un PID clásico, demostrando una reducción significativa en los índices de error IAE e ITAE.

 Estructura del Repositorio


`src/`: Código fuente del controlador en Texto Estructurado (SCL) para PLC S7-1200.


`simulink/`: Modelos matemáticos no lineales y scripts de linealización en MATLAB/Simulink.

 
`factoryio/`: Escena personalizada de Factory I/O con el acoplamiento virtual de los tanques.


`data/`: Archivos CSV con los datos experimentales y comparativas de sintonización.



 Dependencias y Requisitos

TIA Portal V15** (o superior) para la programación del PLC S7-1200.


 Factory I/O** para la simulación de la planta industrial.

MATLAB R2021a** (o superior) con:
Control System Toolbox (para el diseño LQR/LQG).

Simulink (para validación del modelo teórico).


 Cómo utilizar

1. Modelado: Ejecute los scripts en MATLAB para obtener las matrices de ganancia $K$ y de Kalman $L$ basadas en el punto de operación deseado.


2. Simulación: Abra la escena en Factory I/O y configure la comunicación con el PLC (real o simulado vía PLCSIM).


3. Ejecución: Cargue el código SCL del controlador en el PLC. El algoritmo calculará las variables de desviación, realizará la integración de Euler y aplicará la ley de control saturada para proteger la bomba.

