# CLEANSEA

# Especificación de Requerimientos de Software (SRS)

## CLEANSEA — Videojuego de limpieza de cuerpos de agua

**Versión:** 1.0\
**Fecha:** 24 de noviembre de 2026\
**Equipo:**

- Osmar Itiel Murguía Hernández
- Karol Roberto Navarro Urzúa

**Materia:** Introducción a la Ingeniería de Software\

---

# Tabla de contenido

1. Introducción
2. Descripción general
3. Requerimientos funcionales
4. Requerimientos no funcionales
5. Interfaces externas
6. Reglas del juego
7. Restricciones y aspectos pendientes

---

# 1. Introducción

## 1.1 Propósito

Este documento establece los requerimientos funcionales y no funcionales del videojuego **CLEANSEA**. Describe sus características, mecánicas, progresión, interfaces y condiciones técnicas que deberá cumplir durante su desarrollo.

Está dirigido al equipo de desarrollo y al personal académico encargado de evaluar el proyecto.

## 1.2 Alcance

**CLEANSEA** es un videojuego educativo y recreativo en el que el jugador controla a un personaje que explora diferentes cuerpos de agua con el objetivo de recolectar basura y reducir la contaminación de cada escenario.

El jugador podrá vender los residuos recolectados, obtener dinero y utilizarlo para comprar mejoras que faciliten la exploración y limpieza de los escenarios.

El videojuego contará inicialmente con cinco escenarios, cada uno con diferentes características y distribución de residuos.

### Funciones incluidas

- Exploración y movimiento del personaje dentro de los cuerpos de agua.
- Recolección de basura mediante interacción.
- Sistema de inventario con capacidad limitada.
- Clasificación de basura por tipo, tamaño y rareza.
- Venta de basura a cambio de dinero.
- Recompensas económicas por completar escenarios.
- Compra y mejora de habilidades y equipamiento.
- Medición del porcentaje de limpieza.
- Desbloqueo de nuevos escenarios.
- Regreso a escenarios anteriores.
- Sistema de oxígeno para controlar el tiempo de exploración.
- Guardado automático del progreso.
- Menús de navegación y configuración.
- Tutorial inicial.

### Funciones excluidas

- Modo multijugador.
- Compras con dinero real.
- Rankings en línea.
- Editor de niveles.
- Funciones que requieran conexión a internet.

## 1.3 Definiciones, acrónimos y abreviaturas

| Término                | Definición                                                                     |
| ---------------------- | ------------------------------------------------------------------------------ |
| Cuerpo de agua         | Río, lago, laguna o mar que el jugador deberá limpiar.                         |
| Escenario              | Nivel del videojuego que representa un cuerpo de agua específico.              |
| Basura                 | Objeto recolectable que representa un residuo contaminante.                    |
| Basura orgánica        | Residuos de origen orgánico.                                                   |
| Basura inorgánica      | Residuos de origen inorgánico.                                                 |
| Porcentaje de limpieza | Proporción de basura retirada respecto al total considerado para el escenario. |
| Umbral de avance       | Porcentaje mínimo de limpieza necesario para desbloquear otro escenario.       |
| Inventario             | Espacio disponible para almacenar los residuos recolectados.                   |
| Mejora                 | Elemento comprable que aumenta las capacidades del personaje.                  |
| Oxígeno                | Recurso que determina el tiempo de permanencia bajo el agua.                   |
| Moneda                 | Dinero virtual obtenido mediante la venta de basura y recompensas.             |
| HUD                    | Interfaz que muestra información durante la partida.                           |
| Pygame                 | Biblioteca de Python utilizada para desarrollar videojuegos.                   |
| SRS                    | Software Requirements Specification.                                           |
| RF                     | Requerimiento funcional.                                                       |
| RNF                    | Requerimiento no funcional.                                                    |

## 1.4 Referencias

- IEEE Std 830-1998.
- ISO/IEC/IEEE 29148, ingeniería de requerimientos.
- Lineamientos académicos del proyecto.
- Documentación oficial de Python.
- Documentación de Pygame.

---

# 2. Descripción general

## 2.1 Perspectiva del producto

Río Limpio será un videojuego independiente desarrollado utilizando Python y la biblioteca Pygame.

No dependerá de otros sistemas para su funcionamiento y estará diseñado para ejecutarse sin conexión a internet.

El progreso se conservará mediante un sistema de guardado automático.

### Plataformas objetivo

| Plataforma | Orientación |
| ---------- | ----------- |
| PC         | Horizontal  |
| Android    | Vertical    |

El videojuego tendrá una interfaz adaptada a cada plataforma.

## 2.2 Funciones principales

El funcionamiento del videojuego estará basado en el siguiente ciclo:

**Explorar → Recolectar basura → Almacenar → Vender → Comprar mejoras → Limpiar escenarios → Avanzar.**

Las funciones principales serán:

1. Controlar el movimiento del personaje.
2. Explorar los diferentes cuerpos de agua.
3. Recoger basura mediante interacción.
4. Almacenar residuos dependiendo de la capacidad del bolso.
5. Vender los objetos recolectados en tiendas.
6. Obtener dinero adicional al completar escenarios.
7. Comprar mejoras para aumentar las capacidades del personaje.
8. Consultar el porcentaje de limpieza.
9. Desbloquear nuevos escenarios al alcanzar el 80% de limpieza.
10. Regresar a escenarios anteriores para continuar recolectando basura.
11. Guardar automáticamente el progreso.

## 2.3 Características de los usuarios

- **Perfil:** jugadores casuales.
- **Edad aproximada:** de 8 a 35 años (pendiente de confirmar).
- **Experiencia:** no se requiere experiencia previa en videojuegos.
- **Idioma:** español.
- **Duración estimada de las sesiones:** entre 10 y 20 minutos.
- **Plataformas:** PC y Android.

## 2.4 Restricciones

- Lenguaje de programación: Python.
- Biblioteca de desarrollo: Pygame.
- Herramientas de desarrollo: Visual Studio Code y GitHub.
- Estilo gráfico: pixel art de 64 bits.
- Orientación horizontal en PC.
- Orientación vertical en Android.
- El videojuego deberá funcionar sin conexión a internet.
- Se buscará que pueda ejecutarse en dispositivos de bajos recursos.
- El objetivo de rendimiento será de 60 FPS.
- Los recursos gráficos y de audio deberán ser propios o contar con licencias que permitan su utilización.

## 2.5 Suposiciones y dependencias

- El jugador contará con un dispositivo compatible con el videojuego.
- El juego no dependerá de servicios externos para funcionar.
- Se utilizará Python y Pygame como base del desarrollo.
- Se contempla la adaptación de controles e interfaces para PC y Android.
- Se buscará utilizar música libre de derechos de autor o con licencias adecuadas.
- La compatibilidad con Android dependerá de las herramientas adicionales de empaquetado y adaptación que se seleccionen.

## 2.6 Progresión del videojuego

El videojuego contará inicialmente con cinco escenarios.

Cada escenario tendrá una cantidad y distribución de basura propias.

El jugador podrá desbloquear el siguiente escenario cuando alcance un porcentaje de limpieza del 80%.

El jugador también podrá regresar a escenarios anteriores para continuar limpiándolos.

Al alcanzar el 100% de limpieza, recibirá una recompensa económica adicional. Ocasionalmente, podrá generarse basura nuevamente.

Cuando esto ocurra, el porcentaje de limpieza no podrá disminuir por debajo del 80%.

---

# 3. Requerimientos funcionales

Los siguientes requerimientos describen las acciones y funciones que deberá realizar el videojuego.

| ID    | Descripción                                                                                              | Prioridad | Criterio de aceptación                                                                                                        |
| ----- | -------------------------------------------------------------------------------------------------------- | --------- | ----------------------------------------------------------------------------------------------------------------------------- |
| RF-01 | El jugador podrá desplazarse por el escenario utilizando los controles correspondientes a su plataforma. | Alta      | El personaje responde correctamente a las flechas del teclado o botones de pantalla.                                          |
| RF-02 | El jugador podrá explorar libremente el cuerpo de agua dentro de los límites establecidos del mapa.      | Alta      | El personaje puede desplazarse por las zonas permitidas sin salir de los límites.                                             |
| RF-03 | El jugador podrá recolectar basura acercándose a un objeto y presionando un botón de interacción.        | Alta      | El objeto desaparece del escenario y se incorpora al inventario cuando existe espacio suficiente.                             |
| RF-04 | El sistema identificará los diferentes tipos de basura presentes en el escenario.                        | Alta      | Los residuos pueden clasificarse según su categoría y características.                                                        |
| RF-05 | El sistema asignará un valor económico a cada objeto según su tamaño, tipo y rareza.                     | Alta      | Los objetos tienen valores correspondientes a sus características.                                                            |
| RF-06 | El sistema administrará un inventario con capacidad limitada.                                            | Alta      | El jugador no puede almacenar objetos cuando no existe espacio suficiente.                                                    |
| RF-07 | El jugador podrá vender la basura recolectada en tiendas de recolección.                                 | Alta      | Al realizar una venta, se calcula el valor de los objetos y se actualiza el dinero disponible.                                |
| RF-08 | El sistema otorgará una recompensa económica adicional al completar un escenario.                        | Media     | Al alcanzar el 100% de limpieza se entrega la recompensa correspondiente.                                                     |
| RF-09 | El jugador podrá comprar mejoras utilizando el dinero obtenido.                                          | Alta      | Si cuenta con dinero suficiente, la compra se realiza y se descuenta el costo.                                                |
| RF-10 | El sistema permitirá mejorar las capacidades del personaje.                                              | Alta      | Las mejoras adquiridas modifican las características correspondientes.                                                        |
| RF-11 | Las mejoras tendrán hasta tres niveles inicialmente.                                                     | Media     | El jugador podrá adquirir mejoras hasta alcanzar el nivel máximo establecido.                                                 |
| RF-12 | El sistema administrará el oxígeno disponible del personaje.                                             | Alta      | El oxígeno disminuye durante la exploración bajo el agua.                                                                     |
| RF-13 | El sistema aplicará una penalización cuando el oxígeno llegue a cero.                                    | Alta      | El personaje se desmaya, pierde la basura almacenada y una cantidad de dinero por el servicio de rescate.                     |
| RF-14 | El sistema calculará y mostrará el porcentaje de limpieza del escenario.                                 | Alta      | El porcentaje corresponde a la cantidad de basura retirada respecto al total considerado.                                     |
| RF-15 | El sistema desbloqueará el siguiente escenario al alcanzar el 80% de limpieza.                           | Alta      | Al alcanzar el porcentaje requerido, el siguiente escenario queda disponible.                                                 |
| RF-16 | El jugador podrá regresar a escenarios anteriores que ya haya desbloqueado.                              | Media     | El jugador puede seleccionar y acceder a cualquier escenario previamente desbloqueado.                                        |
| RF-17 | El sistema permitirá que aparezca basura nuevamente en escenarios completados.                           | Media     | Puede generarse basura adicional sin reducir el porcentaje de limpieza por debajo del 80%.                                    |
| RF-18 | El sistema guardará automáticamente el progreso después de acciones importantes.                         | Alta      | El progreso se guarda después de vender, comprar mejoras, desbloquear escenarios, completar escenarios y recibir recompensas. |
| RF-19 | El sistema cargará la información guardada al iniciar una nueva sesión.                                  | Alta      | Se recuperan los datos correspondientes al último guardado válido.                                                            |
| RF-20 | El videojuego contará con un menú principal.                                                             | Alta      | El menú permite acceder a Jugar, Créditos, Salir y Configuración.                                                             |
| RF-21 | El videojuego contará con un tutorial inicial.                                                           | Media     | El tutorial explica las acciones básicas necesarias para comenzar a jugar.                                                    |
| RF-22 | El sistema mostrará información relevante durante la partida.                                            | Alta      | Se muestra el dinero disponible, el porcentaje de limpieza y los botones de interacción.                                      |
| RF-23 | El sistema contará con tiendas para adquirir diferentes mejoras.                                         | Media     | El jugador puede acceder a las tiendas y consultar las mejoras disponibles.                                                   |
| RF-24 | El sistema permitirá administrar los diferentes tipos de mejoras.                                        | Media     | Las mejoras de almacenamiento, oxígeno, velocidad, alcance y profundidad afectan sus capacidades correspondientes.            |

## 3.1 Sistema de mejoras

El videojuego contará inicialmente con cinco categorías de mejoras.

| Mejora         | Función                                                         |
| -------------- | --------------------------------------------------------------- |
| Almacenamiento | Aumenta la capacidad del bolso para guardar basura.             |
| Oxígeno        | Aumenta el tiempo disponible para permanecer bajo el agua.      |
| Velocidad      | Aumenta la velocidad de desplazamiento del personaje.           |
| Alcance        | Aumenta la distancia desde la que se pueden recolectar objetos. |
| Profundidad    | Permite explorar zonas más profundas de los cuerpos de agua.    |

Todas las mejoras tendrán hasta tres niveles inicialmente.

Los precios y los valores exactos de mejora estarán sujetos al balance del videojuego.

## 3.2 Sistema de recolección y economía

Los residuos tendrán características que determinarán su valor:

- Tipo de basura.
- Tamaño del objeto.
- Rareza.

La distribución de residuos dependerá del escenario. Algunos cuerpos de agua podrán contener una mayor cantidad de determinados tipos de basura.

La basura recolectada ocupará espacio en el inventario dependiendo de sus características.

El jugador podrá vender los residuos en tiendas especializadas y obtener dinero para comprar mejoras.

También recibirá recompensas económicas al completar escenarios.

## 3.3 Sistema de oxígeno

El personaje tendrá una cantidad limitada de oxígeno para permanecer bajo el agua.

Al agotarse, se desmayará y se aplicarán las siguientes penalizaciones:

- Pérdida de toda la basura almacenada.
- Descuento de algunas monedas por el servicio de rescate.

La cantidad exacta de oxígeno, el costo del rescate y las condiciones de recuperación estarán pendientes de establecerse.

---

# 4. Requerimientos no funcionales

Los requerimientos no funcionales establecen las condiciones de calidad, rendimiento y funcionamiento que deberá cumplir el videojuego.

| ID     | Categoría                  | Descripción                                                                                         | Prioridad | Criterio de aceptación                                                                                                    |
| ------ | -------------------------- | --------------------------------------------------------------------------------------------------- | --------- | ------------------------------------------------------------------------------------------------------------------------- |
| RNF-01 | Rendimiento                | El videojuego deberá buscar un rendimiento estable de 60 FPS.                                       | Alta      | Mantiene aproximadamente 60 FPS en los dispositivos de referencia definidos para las pruebas.                             |
| RNF-02 | Usabilidad                 | El videojuego deberá ser fácil de entender para jugadores sin experiencia previa.                   | Alta      | Un usuario nuevo puede realizar las acciones básicas mediante el tutorial sin ayuda externa.                              |
| RNF-03 | Compatibilidad             | El videojuego deberá funcionar en PC y Android.                                                     | Alta      | Se ejecuta correctamente en las plataformas objetivo definidas.                                                           |
| RNF-04 | Confiabilidad              | El progreso deberá conservarse mediante guardado automático.                                        | Alta      | Después de cerrar y volver a abrir el juego, se recuperan los datos del último guardado válido.                           |
| RNF-05 | Mantenibilidad             | El código deberá organizarse para facilitar modificaciones y la incorporación de nuevos escenarios. | Media     | Es posible agregar escenarios mediante la configuración de sus datos sin modificar innecesariamente la lógica principal.  |
| RNF-06 | Portabilidad               | El videojuego deberá adaptar su interfaz a las características de cada plataforma.                  | Alta      | La interfaz se muestra correctamente en orientación vertical en Android y horizontal en PC.                               |
| RNF-07 | Disponibilidad             | El videojuego deberá funcionar sin conexión a internet.                                             | Alta      | Las funciones principales pueden utilizarse sin conexión.                                                                 |
| RNF-08 | Compatibilidad de hardware | El videojuego deberá estar optimizado para funcionar en computadoras de bajos recursos.             | Alta      | Las pruebas en el equipo mínimo definido permiten ejecutar las funciones principales sin problemas graves de rendimiento. |
| RNF-09 | Integridad de datos        | Los datos del jugador deberán conservarse correctamente durante los procesos de guardado y carga.   | Alta      | Los datos recuperados coinciden con los del último guardado válido.                                                       |
| RNF-10 | Recursos multimedia        | Los recursos de audio y gráficos deberán contar con permisos de utilización adecuados.              | Media     | Los recursos utilizados son propios, libres de derechos o cuentan con licencias compatibles con el proyecto.              |

---

# 5. Interfaces externas

## 5.1 Interfaz de usuario

El videojuego utilizará un estilo gráfico pixel art de 64 bits.

La interfaz deberá adaptarse a las características de cada plataforma.

### Menú principal

El menú principal contará con las siguientes opciones:

| Opción        | Función                                                                 |
| ------------- | ----------------------------------------------------------------------- |
| Jugar         | Iniciar una partida o continuar el progreso.                            |
| Créditos      | Mostrar información sobre los integrantes y colaboradores del proyecto. |
| Salir         | Cerrar el videojuego.                                                   |
| Configuración | Acceder a las opciones disponibles del juego.                           |

### Interfaz durante la partida (HUD)

Durante la partida se mostrarán los siguientes elementos:

- Dinero disponible.
- Porcentaje de limpieza.
- Botones de interacción.

La distribución visual definitiva estará pendiente de diseño.

### Orientación de pantalla

- **Android:** orientación vertical.
- **PC:** orientación horizontal.

## 5.2 Interfaz de controles

| Plataforma | Controles                                          |
| ---------- | -------------------------------------------------- |
| PC         | Flechas del teclado y botones de interacción.      |
| Android    | Botones en pantalla para movimiento e interacción. |

El personaje podrá desplazarse libremente dentro de los límites del escenario.

## 5.3 Interfaz de audio

El videojuego contará con:

- Efectos de sonido para las interacciones.
- Música ambiental durante los escenarios.
- Música permanente en la pantalla de inicio.

Se buscará utilizar música sin restricciones de derechos de autor o con licencias que permitan su uso.

---

# 6. Reglas del juego

## 6.1 Reglas de recolección

1. El jugador deberá acercarse a un objeto de basura.
2. Deberá presionar el botón de interacción para recogerlo.
3. El objeto se almacenará en el inventario si existe espacio suficiente.
4. Cada objeto ocupará una cantidad determinada de espacio.
5. Si el inventario está lleno, no será posible recoger más basura hasta liberar espacio.

## 6.2 Reglas de venta

1. El jugador deberá acudir a una tienda de recolección.
2. Podrá vender la basura almacenada.
3. El dinero recibido dependerá del tipo, tamaño y rareza de los objetos.
4. Después de una venta, el inventario correspondiente quedará liberado.

## 6.3 Reglas de mejoras

1. Las mejoras se adquirirán en diferentes tiendas.
2. Se utilizará el dinero disponible para realizar las compras.
3. Si el jugador no cuenta con dinero suficiente, la compra no podrá realizarse.
4. Cada mejora podrá alcanzar hasta tres niveles inicialmente.
5. Las mejoras modificarán las capacidades correspondientes del personaje.

## 6.4 Reglas de oxígeno

1. El oxígeno será un recurso limitado durante la exploración bajo el agua.
2. Al agotarse, el personaje se desmayará.
3. El jugador perderá la basura que tenga almacenada.
4. Se descontará una cantidad de dinero por el servicio de rescate.

## 6.5 Reglas de progresión

1. El videojuego contará inicialmente con cinco escenarios.
2. Cada escenario tendrá sus propias características y distribución de basura.
3. Al alcanzar el 80% de limpieza, se desbloqueará el siguiente escenario.
4. El jugador podrá regresar a escenarios anteriores.
5. Al alcanzar el 100% de limpieza, recibirá una recompensa económica adicional.
6. En ocasiones podrá aparecer basura nuevamente.
7. La regeneración de basura no reducirá el porcentaje de limpieza por debajo del 80%.

## 6.6 Reglas de guardado

El videojuego realizará guardados automáticos después de las siguientes acciones:

- Vender basura.
- Comprar mejoras.
- Desbloquear un escenario.
- Completar un escenario.
- Recibir recompensas.

La información que deberá conservarse será:

- Dinero disponible.
- Mejoras compradas y sus niveles.
- Escenarios desbloqueados.
- Porcentaje de limpieza de cada escenario.
- Inventario actual.

El guardado no se realizará simplemente por sumergirse en el agua.

---

# 7. Restricciones y aspectos pendientes

Los siguientes aspectos todavía necesitan ser definidos por el equipo antes de considerar completamente cerrada la especificación.

| ID   | Aspecto pendiente      | Descripción                                                                  |
| ---- | ---------------------- | ---------------------------------------------------------------------------- |
| P-01 | Resolución             | Definir las resoluciones objetivo para PC y Android.                         |
| P-02 | Compatibilidad Android | Definir la versión mínima y el método de empaquetado del videojuego.         |
| P-03 | Hardware mínimo        | Establecer los requisitos mínimos de memoria, procesador y gráficos.         |
| P-04 | Guardado               | Definir el formato y la ubicación de almacenamiento de los datos.            |
| P-05 | HUD                    | Diseñar la distribución definitiva de los elementos de interfaz.             |
| P-06 | Economía               | Establecer los precios de los objetos, mejoras y recompensas.                |
| P-07 | Inventario             | Definir la capacidad inicial y el espacio ocupado por cada objeto.           |
| P-08 | Oxígeno                | Definir la duración inicial y los valores de las mejoras.                    |
| P-09 | Penalizaciones         | Establecer la cantidad de monedas descontadas por rescate.                   |
| P-10 | Escenarios             | Definir los nombres, características y dificultades de los cinco escenarios. |
| P-11 | Regeneración           | Definir la frecuencia y cantidad de basura que podrá reaparecer.             |
| P-12 | Música                 | Seleccionar los recursos musicales y sus licencias.                          |

## 7.1 Consideración técnica

Pygame está orientado principalmente al desarrollo de videojuegos para PC. Por lo tanto, la ejecución en Android representa un aspecto técnico que deberá investigarse y comprobarse mediante pruebas de compatibilidad y empaquetado.

## 7.2 Consideración sobre el rendimiento

Los 60 FPS representan el objetivo de rendimiento del proyecto. Será necesario realizar pruebas en los dispositivos de referencia para comprobar que se alcanza una fluidez adecuada, especialmente en equipos de bajos recursos.

---

**Fin del documento SRS — Río Limpio**

*Versión 1.0 — 24 de noviembre de 2026*
