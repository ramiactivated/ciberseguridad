🛡️ Cybersecurity & Systems Lab
Bienvenido a mi repositorio personal de prácticas y recursos de ciberseguridad. Este espacio está diseñado para documentar mi aprendizaje y evolución en diferentes áreas de la seguridad informática, desde el bastionado de sistemas hasta la ejecución de auditorías éticas.

📁 Estructura del Repositorio
El contenido está organizado por áreas temáticas siguiendo el plan de estudios y mis investigaciones personales:

[Bastionado](Bationado): Configuración y endurecimiento de sistemas operativos y servicios para reducir la superficie de ataque.

[Forense](Forense): Análisis de evidencias digitales, recuperación de datos y respuesta ante incidentes.

[Hacking](Hacking): Pruebas de penetración, explotación de vulnerabilidades y técnicas ofensivas (CTFs y laboratorios).

[Maletín de Herramientas](Maletin_Herramientas): Recopilación de scripts, utilidades y comandos esenciales para el día a día.

[Normativa](Normativa): Documentación sobre marcos legales, cumplimiento (GDPR, ENS) y estándares de seguridad.

[Puesta en Producción](Puestaenproduccion): Despliegue seguro de aplicaciones y gestión de entornos de sistemas.

[Metodología](metodologia.md): Guías paso a paso y frameworks (como OWASP o PTES) utilizados en mis auditorías.

🛠️ Tecnologías y Herramientas

Sistemas y Bastionado
Sistemas Operativos:
Hardening: SSH Hardening, Configuración de Firewalls (UFW, IPTables), Políticas de Grupo (GPO).

Seguridad Ofensiva (Hacking) y Forense
Análisis de Red: Nmap, Bettercap.

Explotación: Metasploit Framework, Burp Suite, John the Ripper, Hashcat.

Forense: Autopsy, Volatility, FTK Imager.

Infraestructura y Despliegue (Puesta en Producción)
Contenedores:
Servidores Web: Nginx, Apache.

## ⚡ Comandos Potentes (One-Liners)
<details>
<summary>📂 <b>Ver comandos de</b></summary>
Esta es una selección de comandos avanzados para agilizar tareas de pentesting, forense y administración de sistemas.

🔍 Reconocimiento y Redes
Identificar dispositivos vivos en la red local (Ping Sweep):

Bash

for i in {1..254}; do ping -c 1 -W 1 192.168.1.$i | grep "from" & done
Listar todos los subdominios de un sitio (usando crt.sh):

Bash

curl -s https://crt.sh/\?q\=%25.google.com\&output\=json | jq -r '.[].name_value' | sed 's/\*\.//g' | sort -u
Captura rápida de tráfico en el puerto 80 (HTTP):

Bash

sudo tcpdump -i eth0 port 80 -A

🛡️ Auditoría y Escalada de Privilegios
Buscar archivos con permisos de escritura para "otros" (World-Writable):

Bash

find / -perm -o+w -type f 2>/dev/null | grep -v "/proc"

Encontrar archivos editados en los últimos 10 minutos (ideal para detectar cambios recientes):

Bash

find / -mmin -10 -type f 2>/dev/null

Ver capacidades especiales de archivos (Capabilities):

Bash

getcap -r / 2>/dev/null


🕵️ Análisis de Logs y Forense

Monitorizar intentos de acceso fallidos por SSH en tiempo real:
Bash

tail -f /var/log/auth.log | grep "Failed password"

Contar cuántas peticiones ha hecho cada IP a tu servidor web:

Bash

awk '{print $1}' /var/log/apache2/access.log | sort | uniq -c | sort -nr

Extraer metadatos básicos de un archivo (sin instalar exiftool):

Bash

strings [archivo] | head -n 20


⚙️ Gestión de Sistemas y Servicios

Matar todos los procesos de un usuario específico:

Bash

pgrep -u [usuario] | xargs kill -9

Saber qué proceso está escuchando en un puerto específico:

Bash

sudo lsof -i :80

Ver el consumo de recursos de los contenedores Docker en tiempo real:

Bash

docker stats --no-stream --format "table {{.Name}}\t{{.CPUPerc}}\t{{.MemUsage


</details>




🚀 Objetivos
Documentar la resolución de máquinas y laboratorios.

Crear una base de conocimiento sólida para consultas rápidas.

Compartir metodologías de trabajo en entornos de Pentesting.
