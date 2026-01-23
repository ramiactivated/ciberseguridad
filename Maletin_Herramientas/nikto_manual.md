# ⚡ Manual de Uso: Nikto

> Escáner de servidores web para detectar archivos peligrosos, CGIs y software desactualizado.

### 💻 Ejemplo de Uso Real

```bash
# Escaneo de un servidor seguro (SSL) en puerto alternativo, buscando solo ficheros (rápido)
nikto -h target.com -p 8443 -ssl -Tuning 1 -o reporte.html -Format html

-h : Define el Host o escaneo básico del servidor objetivo.

-p [puerto] : Especifica un puerto diferente al estándar (ej: -p 8080 o -p 8443).

-ssl : Fuerza el escaneo a través de HTTPS (útil si el puerto 443 no se detecta automáticamente).

-Tuning [n] : Ajuste de escaneo. Filtra qué tipo de vulnerabilidades buscar:

1: Ficheros interesantes (El más rápido).

4: Inyección XSS.

9: SQL Injection.

-o [archivo] -Format html : Guarda el informe detallado en un archivo con formato HTML.

-delay [segundos] : Introduce una pausa entre peticiones para evitar bloqueos de seguridad (WAF) o no saturar el servidor.
