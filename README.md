# **Universidad del Cauca - Facultad de Ingeniería Electrónica y Telecomunicaciones - Programa de ingeniería de sistemas Ingeniería de Software II - Laboratorio de Ingeniería de Software II - Julio Ariel Hurtado, Pablo Magé, W. Libardo Pantoja**
# ProyectoSoftwareII
# Planteamiento del problema
Las pruebas Saber Pro constituyen uno de los principales mecanismos para evaluar las competencias adquiridas por los estudiantes de educación superior en Colombia. En
consecuencia, las instituciones universitarias desarrollan estrategias para fortalecer la preparación de sus estudiantes mediante simulacros, bancos de preguntas y actividades de entrenamiento.
Sin embargo, la construcción de un banco de preguntas de calidad representa un proceso complejo. En muchas ocasiones, las preguntas son elaboradas de forma aislada por
diferentes docentes, sin seguir criterios homogéneos de redacción, estructura o validación.
Esto ocasiona problemas como preguntas ambiguas, distractores poco plausibles, inconsistencias entre el contexto y la pregunta, errores conceptuales y ausencia de procesos
de revisión que garanticen la calidad de los ítems.
Adicionalmente, la mayoría de herramientas disponibles se enfocan únicamente en almacenar preguntas y presentar cuestionarios, dejando de lado aspectos fundamentales
como la administración del ciclo de vida de una pregunta, la revisión por pares, la trazabilidad de las modificaciones, la aplicación de criterios de calidad, el seguimiento del desempeño de los estudiantes y la obtención de indicadores que apoyen el mejoramiento continuo del banco
de preguntas.
Por esta razón, surge la necesidad de desarrollar un sistema de información que permita gestionar integralmente el proceso de creación, validación, administración y utilización de preguntas para la preparación de las pruebas Saber Pro, incorporando mecanismos que aseguren la calidad de los ítems y faciliten su reutilización en simulacros de evaluación.
# Objetivo general
Desarrollar un sistema web para la gestión integral de un banco de preguntas orientado a la preparación de estudiantes para las pruebas Saber Pro, permitiendo administrar el ciclo de vida de las preguntas, garantizar su calidad mediante procesos de revisión por pares y
facilitar la generación de simulacros de evaluación.

# Requerimientos funcionales
## HU01. Gestión de usuarios del sistema
- RF-01. El sistema deberá permitir registrar usuarios que interactúan con la aplicación.
- RF-02. El sistema deberá permitir autenticación mediante usuario y contraseña.
- RF-03. El sistema deberá administrar diferentes roles:
 ● Administrador
 ● Autor de preguntas
 ● Revisor
 ● Docente
 ● Estudiante
## HU02. Gestión del banco de preguntas
- RF-04. El sistema deberá permitir crear preguntas.
- RF-05. Cada pregunta deberá estar conformada por:
 ● Contexto
 ● Pregunta directa
 ● Cuatro distractores
 ● Respuesta correcta
 ● Justificación de la respuesta
 ● Bibliografía
 ● Competencia
 ● Tema
 ● Subtema
 ● Nivel de dificultad
- RF-06. El sistema deberá permitir modificar preguntas mientras se encuentren en estado
"Borrador".
- RF-07. El sistema deberá permitir consultar preguntas mediante filtros.
## HU03. Validación estructural
- RF-08. El sistema deberá validar automáticamente que toda pregunta contenga un contexto.
- RF-09. El sistema deberá validar que exista una única pregunta directa.
- RF-10. El sistema deberá verificar que existan exactamente cuatro distractores.
- RF-11. El sistema deberá validar que exista únicamente una respuesta correcta.
- RF-12. El sistema deberá impedir el uso de expresiones como:
 ● Todas las anteriores
 ● Ninguna de las anteriores
- RF-13. El sistema deberá verificar que los distractores respeten criterios básicos de longitud
y estructura gramatical.
## HU04. Gestión del ciclo de vida
- RF-14. El sistema deberá administrar los siguientes estados de una pregunta:
 ● Borrador
 ● Pendiente de revisión
 ● En revisión
 ● Aprobada
 ● Rechazada
 ● Publicada
 ● Archivada
- RF-15. El sistema deberá controlar las transiciones válidas entre estados.
## HU05. Revisión por pares.
- RF-16. El sistema deberá permitir asignar revisores a una pregunta.
- RF-17. Cada revisor deberá diligenciar un formato de evaluación.
- RF-18. El sistema deberá registrar observaciones realizadas por los revisores.
- RF-19. El sistema deberá almacenar el historial de revisiones.
- RF-20. El sistema deberá permitir aprobar o rechazar una pregunta.
## HU06. Simulacros
- RF-21. El sistema deberá permitir generar simulacros utilizando preguntas publicadas.
- RF-22. El sistema deberá generar simulacros aleatorios de acuerdo con competencias, temas o niveles de dificultad.
- RF-23. El sistema deberá controlar el tiempo máximo del simulacro.
- RF-24. El sistema deberá calificar automáticamente las respuestas.
## HU07. Seguimiento académico
- RF-25. El sistema deberá almacenar el historial de simulacros realizados por cada estudiante.
- RF-26. El sistema deberá generar estadísticas individuales.
- RF-27. El sistema deberá identificar fortalezas y debilidades por competencia.
- RF-28. El sistema deberá generar reportes para docentes y coordinadores.
## HU08. Administración
- RF-29. El sistema deberá mantener la trazabilidad de todas las modificaciones realizadas a una pregunta.
- RF-30. El sistema deberá registrar la fecha y el usuario responsable de cada modificación.
# Requerimientos no funcionales
## Usabilidad
- RNF-01. La interfaz deberá ser intuitiva y consistente.
- RNF-02. El sistema deberá ser accesible desde navegadores web modernos.
- RNF-03. La curva de aprendizaje para un usuario nuevo no deberá superar treinta minutos.
## Rendimiento
- RNF-04. El sistema deberá responder una consulta en menos de tres segundos bajo
- condiciones normales.
- RNF-05. El sistema deberá soportar al menos cien usuarios concurrentes.
## Seguridad
- RNF-06. El sistema deberá implementar autenticación de usuarios.
- RNF-07. El sistema deberá restringir el acceso según el rol del usuario.
- RNF-08. Todas las contraseñas deberán almacenarse utilizando algoritmos de hash seguros.
- RNF-09. El sistema deberá registrar los eventos relevantes de auditoría, como inicio de sesión, cambios de estado de las preguntas y acciones de revisión.
## Modificabilidad
- RNF-10. El código fuente deberá seguir principios SOLID y buenas prácticas de diseño orientado a objetos.
- RNF-11. La arquitectura deberá facilitar el mantenimiento y la incorporación de nuevos módulos.
- RNF-12. El sistema deberá mantener separación entre la lógica de negocio, la interfaz de usuario y la persistencia.
- RNF-13. La arquitectura deberá permitir incorporar nuevos tipos de preguntas, nuevos criterios de revisión, nuevas competencias y nuevos módulos sin requerir cambios significativos en los componentes existentes.
- RNF-14. El sistema deberá favorecer un bajo acoplamiento y una alta cohesión entre sus componentes, facilitando su mantenimiento y evolución.
## Confiabilidad
- RNF-15. El sistema deberá garantizar la integridad de la información almacenada.
- RNF-16. Ninguna pregunta podrá eliminarse físicamente; únicamente podrá cambiar a un
- estado de inactiva o archivada, preservando la trazabilidad del banco de preguntas.
## Escalabilidad
- RNF-17. El sistema deberá soportar al menos 500 usuarios concurrentes manteniendo un tiempo promedio de respuesta inferior a 3 segundos para las operaciones de consulta.
RNF-18. La arquitectura deberá permitir incrementar la capacidad del sistema mediante la incorporación de nuevos recursos de hardware o instancias de ejecución sin requerir
modificaciones en la lógica de negocio.
