<div align="center">
  <h1>🛡️ Laboratorio de Ciberseguridad & Sistemas</h1>
  <p><strong>Repositorio personal de prácticas, hardening y pentesting</strong></p>

  <img src="https://img.shields.io/badge/Estado-Activo-success?style=for-the-badge&logo=github">
  <img src="https://img.shields.io/badge/Enfoque-Red_Team_%2F_Blue_Team-red?style=for-the-badge">
</div>

<br>

### 📁 Estructura del Repositorio

El contenido está organizado temáticamente. Haz clic en las carpetas para acceder:

📂 **Raíz del Proyecto**
<br>
├── [**🛡️ Bastionado**](./Bationado)
<br>
│   └── *Hardening, Firewalls (UFW/IPtables) y GPO.*
<br>
├── [**🕵️ Forense**](./Forense)
<br>
│   └── *Análisis de evidencias, Autopsy y Volatility.*
<br>
├── [**💀 Hacking**](./Hacking)
<br>
│   └── *Pentesting, Metasploit, CTFs y Exploits.*
<br>
├── [**🧰 Maletín de Herramientas**](./Maletin_Herramientas)
<br>
│   └── *Scripts, diccionarios y utilidades diarias.*
<br>
├── [**⚖️ Normativa**](./Normativa)
<br>
│   └── *Cumplimiento legal (GDPR, ENS) y estándares.*
<br>
├── [**🚀 Puesta en Producción**](./Puestaenproduccion)
<br>
│   └── *Despliegue seguro, Nginx/Apache y Contenedores.*
<br>
└── [**🧠 Metodología**](./metodologia)
    └── *Guías basadas en OWASP y PTES.*


### 🛠️ Tecnologías y Herramientas

**💀 Seguridad Ofensiva & Red Team**
<p>
  <img src="https://img.shields.io/badge/Kali_Linux-557C94?style=for-the-badge&logo=kali-linux&logoColor=white">
  <img src="https://img.shields.io/badge/Nmap-2D8CFF?style=for-the-badge&logo=nmap&logoColor=white">
  <img src="https://img.shields.io/badge/Bettercap-000000?style=for-the-badge&logo=linux&logoColor=white">
  <br>
  <img src="https://img.shields.io/badge/Metasploit-333333?style=for-the-badge&logo=metasploit&logoColor=white">
  <img src="https://img.shields.io/badge/Burp_Suite-F66A0A?style=for-the-badge&logo=burpsuite&logoColor=white">
  <img src="https://img.shields.io/badge/Hashcat-D40000?style=for-the-badge&logo=cmd&logoColor=white">
  <img src="https://img.shields.io/badge/John_The_Ripper-444444?style=for-the-badge&logo=hackthebox&logoColor=white">
</p>

**🛡️ Bastionado de Sistemas (Hardening)**
<p>
  <img src="https://img.shields.io/badge/Linux_Hardening-FCC624?style=for-the-badge&logo=linux&logoColor=black">
  <img src="https://img.shields.io/badge/SSH-2C2C2C?style=for-the-badge&logo=openssh&logoColor=white">
  <img src="https://img.shields.io/badge/UFW_Firewall-E95420?style=for-the-badge&logo=ubuntu&logoColor=white">
  <img src="https://img.shields.io/badge/Windows_GPO-0078D6?style=for-the-badge&logo=windows&logoColor=white">
</p>

**🕵️ Análisis Forense Digital**
<p>
  <img src="https://img.shields.io/badge/Autopsy-154959?style=for-the-badge&logo=security&logoColor=white">
  <img src="https://img.shields.io/badge/Volatility-000000?style=for-the-badge&logo=python&logoColor=green">
  <img src="https://img.shields.io/badge/FTK_Imager-5B2C6F?style=for-the-badge&logo=database&logoColor=white">
</p>

**🏗️ Infraestructura & Despliegue**
<p>
  <img src="https://img.shields.io/badge/Nginx-009639?style=for-the-badge&logo=nginx&logoColor=white">
  <img src="https://img.shields.io/badge/Apache-D22128?style=for-the-badge&logo=apache&logoColor=white">
  <img src="https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white">
</p>



---

## ⚡ Comandos Potentes (Cheatsheet)
> *Selección de "One-Liners" para agilizar tareas de pentesting, forense y administración.*

<details>
  <summary><b>🔻 HACKER MODE: Desplegar lista de comandos</b> (Click aquí)</summary>
  <br>

### 🔍 Reconocimiento y Redes
```bash
# Identificar hosts vivos en la red (Ping Sweep rápido)
for i in {1..254}; do ping -c 1 -W 1 192.168.1.$i | grep "from" & done

# Enumerar subdominios usando certificados SSL (crt.sh)
curl -s "[https://crt.sh/?q=%.google.com&output=json](https://crt.sh/?q=%.google.com&output=json)" | jq -r '.[].name_value' | sed 's/*.//g' | sort -u

# Sniffing rápido de tráfico HTTP (Puerto 80)
sudo tcpdump -i eth0 port 80 -A


🛡️ Auditoría y Escalada de Privilegios

# Buscar archivos "World-Writable" (peligrosos)
find / -perm -o+w -type f 2>/dev/null | grep -v "/proc"

# Archivos modificados en los últimos 10 min (Detectar intrusiones/cambios)
find / -mmin -10 -type f 2>/dev/null

# Listar capabilities (Permisos especiales de binarios)
getcap -r / 2>/dev/null



🕵️ Análisis de Logs y Forense

# Monitorizar ataques de fuerza bruta SSH en tiempo real
tail -f /var/log/auth.log | grep "Failed password"

# Top IPs que visitan tu servidor web (Ordenadas por cantidad)
awk '{print $1}' /var/log/apache2/access.log | sort | uniq -c | sort -nr

# Extraer strings de un binario/imagen (Análisis rápido sin exiftool)
strings [archivo] | head -n 20





⚙️ Gestión de Sistemas y Servicios

# Matar todos los procesos de un usuario concreto
pgrep -u [usuario] | xargs kill -9

# ¿Qué proceso escucha en el puerto 80?
sudo lsof -i :80

# Monitorizar Docker en tiempo real (Formato tabla limpia)
docker stats --no-stream --format "table {{.Name}}\t{{.CPUPerc}}\t{{.MemUsage}}"



</details>




🚀 Objetivos
Documentar la resolución de máquinas y laboratorios.

Crear una base de conocimiento sólida para consultas rápidas.

Compartir metodologías de trabajo en entornos de Pentesting.
