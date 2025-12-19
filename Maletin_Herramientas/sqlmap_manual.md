Comando / Opción	Qué hace
sqlmap -u "<URL>"	Objetivo básico por URL.
sqlmap -r request.txt	Carga una petición HTTP completa desde un archivo (útil para POST).
--dbs	Enumera todas las bases de datos disponibles.
-D <DB> --tables	Lista las tablas de una base de datos específica.
-T <tabla> --dump	Extrae los datos de una tabla específica.
--batch	Responde automáticamente "sí" a todas las preguntas de confirmación.
--random-agent	Usa un User-Agent aleatorio para evitar bloqueos simples.
