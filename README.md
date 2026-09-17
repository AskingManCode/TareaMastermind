# Proyecto Mastermind

Este proyecto es una implementación interactiva en consola del clásico juego de mesa **Mastermind**, desarrollada como parte de la *Tarea Corta #1* para el curso de Fundamentos de Programación / Programación V.

El objetivo principal de esta tarea es fortalecer el pensamiento lógico, el diseño limpio y la estructuración modular de software utilizando **[Lucia](https://www.lucia-lang.com/)**, un lenguaje de programación desarrollado por nuestro profesor, con sintaxis clara y moderna orientada al aprendizaje y al diseño estructurado. 

En esta versión de Mastermind, el usuario debe adivinar una combinación secreta de 4 colores en un número determinado de intentos, recibiendo pistas mediante fichas negras (posiciones y colores exactos) y fichas blancas (colores correctos en posiciones incorrectas).

## Integrantes.

* Sebastián Jiménez Arrieta.
* Mathiew López Sánchez
* Hector Román Arrieta

## Cómo ejecutar.
### Requisitos e Instalación del Lenguaje Lucia
Para ejecutar el proyecto se requiere el compilador/intérprete o IDE del lenguaje **Lucia**.
1. Descarga el entorno o CLI oficial desde la [página de descargas de Lucia](https://www.lucia-lang.com/download).
2. Puede consultar la [Documentación Oficial de Lucia](https://www.lucia-lang.com/docs) para más detalles sobre la configuración del entorno.

### Instrucciones de Ejecución
1. Clona o descarga el repositorio en tu equipo.
2. Abre una terminal en la raíz del proyecto.
3. Ejecuta el archivo principal `main.lucia` utilizando el intérprete de Lucia:
   ```bash
   main.lucia
   ```
   *(también podría abrir y ejecuta el archivo `main.lucia` directamente desde el editor/IDE de Lucia).*

## Funcionalidades implementadas.

- **Menú Principal e Interactivo:** Flujo interactivo en consola con menú de bienvenida, acceso a instrucciones y opción de salida.
- **Flujo de Configuración Paso a Paso:** Sistema dinámico de configuración que permite avanzar entre pasos (instrucciones, dificultad y cantidad de intentos) o regresar al paso anterior o al menú principal en cualquier momento.
- **Niveles de Dificultad Configurables:**
  - **Nivel Normal:** Genera combinaciones sin repetir colores y sin posiciones vacías.
  - **Nivel Alto:** Permite posiciones vacías en el código secreto y permite al usuario dejar espacios vacíos en sus propuestas (ejemplo: `Rojo,,Verde,Negro`).
- **Personalización de Intentos:** Permite al jugador elegir entre 1 y 15 intentos por partida (con un valor predeterminado de 15 al presionar Enter).
- **Generación Aleatoria de Código Secreto:** Motor que construye combinaciones válidas según la dificultad seleccionada.
- **Lectura y Validación de Propuestas:** Entrada de datos por consola flexible y tolerante a espacios, validando colores permitidos, formato de comas y la opción de rendirse/abandonar la partida tecleando `Salir`.
- **Evaluación y Retroalimentación (Feedback):** Comparación lógica precisa entre el intento y el código secreto, calculando:
  - **Fichas Negras:** Aciertos de color en la posición correcta.
  - **Fichas Blancas:** Aciertos de color en posición incorrecta.
- **Gestión del Estado del Juego (Game Over / Victoria):** Detección automática de victoria al descifrar el código completo (4 fichas negras) o fin de juego por intentos agotados o abandono voluntario.

## Diagrama de clases.
![Diagrama de Clases](<./Documentacion/Diagramas Generales/Diagrama de Clases (Mastermind).drawio.png>) 


## Diagrama de casos de uso.
![Diagrama de Casos de Uso](<./Documentacion/Diagramas Generales/Diagrama de Casos de Uso (Mastermind).drawio.png>)

## Qué mejoras harían en una versión 2.0.

Para una futura versión **2.0** del juego, se proponen las siguientes mejoras técnicas y de experiencia de usuario:
1. **Sistema de Persistencia y Estadísticas (High Scores):** Guardar en un archivo local (JSON/TXT) el historial de partidas, porcentaje de victorias, promedio de intentos empleados y mejores tiempos.
2. **Sistema de Pistas Avanzado:** Implementar un input opcional de "Pista" que consuma un intento extra a cambio de revelar un color o descartar colores no presentes.
3. **Dificultades Adicionales y Personalizables:** Permitir configurar la longitud de la combinación secreta (ej. 5 o 6 posiciones) o incrementar la paleta de colores disponibles.