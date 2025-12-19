Comando / Opción	Qué hace
-h <URL>	Escaneo básico del servidor objetivo.
-p <puerto>	Especifica un puerto diferente al 80/443 (ej: -p 8080).
-ssl	Fuerza el escaneo a través de HTTPS.
-Tuning <número>	Ajuste de escaneo: 1 (Ficheros interesantes), 4 (XSS), 9 (SQL Injection). El tuning 1 es el más rápido.
-o <ruta> -Format html	Guarda el informe detallado en formato HTML.
-delay <segundos>	Introduce una pausa entre peticiones para evitar bloqueos.
