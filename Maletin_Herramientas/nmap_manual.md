Comando / Opción	Qué hace
nmap -sn <IP>	Ping Scan: Solo descubre si el host está vivo, sin escanear puertos.
nmap -sS <IP>	SYN Scan: Escaneo rápido y sigiloso (requiere privilegios de root).
nmap -p- <IP>	Escanea todos los 65,535 puertos (por defecto solo escanea 1,000).
nmap -sV <IP>	Detección de Versión: Intenta identificar qué versión de software corre en el puerto.
nmap -O <IP>	Detección de SO: Intenta adivinar el Sistema Operativo.
nmap -A <IP>	Modo Agresivo: Combina detección de SO, versiones, scripts y traceroute.
nmap --script <nombre>	Ejecuta un script específico del motor NSE (vulnerabilidades, auth, etc.).
