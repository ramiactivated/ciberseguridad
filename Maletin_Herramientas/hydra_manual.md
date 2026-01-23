# 🐲 Manual de Uso: Hydra

> Herramienta de inicio de sesión por fuerza bruta en red (SSH, FTP, HTTP, etc.).

### 💻 Ejemplo de Uso Real

```bash
# Ataque SSH probando múltiples usuarios y contraseñas, parando al primer éxito
hydra -L usuarios.txt -P /usr/share/wordlists/rockyou.txt -t 16 -f ssh://192.168.1.20

-l [nombre] : (l minúscula) Especifica un único nombre de usuario (ej: -l admin).

-L [archivo] : (L mayúscula) Carga una lista de nombres de usuario desde un archivo de texto.

-p [clave] : (p minúscula) Prueba una única contraseña contra todos los usuarios.

-P [archivo] : (P mayúscula) Carga un diccionario de contraseñas (ej: rockyou.txt) para probar masivamente.

-t 16 : Define el número de conexiones en paralelo (hilos). A mayor número, más velocidad, pero más riesgo de saturar el servicio.

-f : Exit on Found. Detiene el ataque inmediatamente en cuanto encuentra la primera credencial válida (ahorra tiempo).

ssh://[IP] : Especifica el protocolo y el objetivo.

Sintaxis: protocolo://ip (Soporta ftp, telnet, mysql, rdp, http-post-form, etc.).
