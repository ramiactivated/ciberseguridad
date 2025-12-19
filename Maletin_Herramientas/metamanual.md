Conceptos Básicos
msfconsole: La interfaz de línea de comandos principal.

Módulos:

exploit: Código que aprovecha una vulnerabilidad.

payload: El código que se ejecuta en el objetivo tras el exploit (ej. una reverse shell).

auxiliary: Escáneres, fuzzers y herramientas de recolección de datos.

post: Módulos para después de comprometer el sistema (escalada de privilegios).

Comandos Esenciales
Bash

msfconsole                     # Iniciar Metasploit
search [nombre]                # Buscar un exploit o módulo
use [ruta_del_modulo]          # Seleccionar un módulo
show options                   # Ver qué datos necesita el exploit
set RHOSTS [IP_objetivo]       # Configurar la IP de la víctima
set LHOST [Tu_IP]              # Configurar tu IP para la conexión reversa
exploit                        # Lanzar el ataque (o 'run' para auxiliares)
