# 💉 Manual de Uso: SQLmap

> Herramienta automática de inyección SQL y toma de control de bases de datos.

### 💻 Ejemplo de Uso Real

```bash
# Ataque a una URL vulnerable intentando evitar bloqueos y aceptando todo por defecto
sqlmap -u "[http://target.com/vuln.php?id=1](http://target.com/vuln.php?id=1)" --random-agent --batch --dbs

-u "URL" : Define el Objetivo básico directo por URL (Petición GET).

-r [archivo] : Carga una petición HTTP completa guardada en un archivo. Esencial para inyecciones en formularios POST o cabeceras.

--dbs : Enumera y lista todas las bases de datos alojadas en el servidor.

-D [nombre] --tables : Dentro de una base de datos específica (-D), lista todas sus tablas.

-T [nombre] --dump : Selecciona una tabla concreta (-T) y extrae (vuelca) todos sus datos en pantalla y archivos .csv.

--batch : Modo automático. Responde "sí" (o la opción por defecto) a todas las preguntas de confirmación del programa.

--random-agent : Cambia la firma del navegador (User-Agent) por una aleatoria para evitar bloqueos de seguridad básicos.
