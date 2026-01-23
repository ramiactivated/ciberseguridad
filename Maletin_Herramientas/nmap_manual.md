# 🗺️ Manual de Uso: Nmap

El estándar de la industria para descubrimiento de redes y auditoría.

### 💻 Ejemplo de Uso Real

```bash
# Escaneo completo sigiloso (SYN), todos los puertos, con versiones y scripts de vuln
sudo nmap -sS -p- -sV -O --script=vuln 192.168.1.10

-sn : Ping Scan. Solo descubre si el host está vivo (online) sin escanear puertos.

-sS : SYN Scan. Escaneo rápido y sigiloso (no completa la conexión TCP). Requiere permisos de root/sudo.

-p- : Escanea todos los 65,535 puertos (por defecto Nmap solo escanea los 1,000 más comunes).

-sV : Detección de Versión. Interroga a los puertos abiertos para identificar el software y su versión exacta.

-O : Detección de SO. Analiza la respuesta de los paquetes para adivinar el Sistema Operativo (Windows, Linux, etc.).

-A : Modo Agresivo. Un "combo" que activa detección de SO, versiones, scripts y traceroute al mismo tiempo.

--script [nombre] : Ejecuta scripts específicos del motor NSE (ej. buscar vulnerabilidades, fuerza bruta, auth).
