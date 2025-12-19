Búsqueda offline en la base de datos de Exploit-DB.

Uso Principal
Permite encontrar vulnerabilidades conocidas sin necesidad de conexión a internet.

Comandos Clave
Buscar un exploit:

Bash

searchsploit windows smb    # Busca exploits para Windows y el protocolo SMB
Examinar un exploit (ver el código):

Bash

searchsploit -x 42315       # Abre el exploit con el ID 42315
Copiar el exploit a tu carpeta actual:

Bash

searchsploit -m 42315       # Crea una copia para que puedas editarla o lanzarla
Actualizar la base de datos:

Bash

searchsploit -u
