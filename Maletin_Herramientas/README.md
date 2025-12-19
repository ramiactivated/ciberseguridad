🧰 Maletín Maestro de Herramientas para Hacking Ético
Este repositorio sirve como base de conocimientos y arsenal de herramientas para auditorías de ciberseguridad y hacking ético.

🔍 1. Reconocimiento y OSINT (Inteligencia de Fuentes Abiertas)
Recopilación de información sobre el objetivo sin interactuar directamente con él.

[theHarvester](theHarvester_manual.md): Herramienta para recolectar correos electrónicos, nombres de subdominios, IPs y nombres de empleados utilizando múltiples fuentes públicas.

Sherlock: Permite buscar nombres de usuario en cientos de sitios de redes sociales para trazar perfiles de presencia digital.

Maltego: Software avanzado para minería de datos y representación gráfica de relaciones entre personas, dominios y redes.

PhoneInfoga: Marco de trabajo avanzado para el escaneo y recopilación de información sobre números de teléfono internacionales.

Shodan: Motor de búsqueda de dispositivos conectados (IoT), cámaras, servidores y bases de datos expuestas en internet.

OSINT Framework: Directorio web masivo que organiza herramientas de investigación por categorías como IP, dominios o correos.

[WhatWeb](whatweb_manual.md): Identificación de tecnologías y versiones de una web.

📡 2. Escaneo de Red y Enumeración
Identificación de puertos abiertos, servicios en ejecución y sistemas operativos.

[Nmap](nmap_manual.md) (Network Mapper): El estándar de la industria para el descubrimiento de hosts, escaneo de puertos y auditoría de seguridad mediante scripts NSE.

Masscan: Considerado el escáner de puertos más rápido, capaz de escanear toda la red Internet en minutos si el ancho de banda lo permite.

Netcat (nc): Conocida como la "navaja suiza de TCP/IP", permite leer y escribir datos a través de conexiones de red de forma manual.

Wireshark: Analizador de protocolos de red que permite capturar e inspeccionar el tráfico en tiempo real a nivel de paquetes.

🌐 3. Auditoría de Aplicaciones Web
Herramientas específicas para encontrar vulnerabilidades en sitios y servicios web.

Burp Suite: Plataforma líder para realizar pruebas de seguridad en aplicaciones web, actuando como un proxy de interceptación.

OWASP ZAP (Zed Attack Proxy): Alternativa de código abierto a Burp Suite, ideal para encontrar vulnerabilidades comunes de forma automatizada.

[SQLmap](sqlmap_manual.md): Herramienta potente para detectar y explotar fallos de inyección SQL y tomar el control de servidores de bases de datos.

[Gobuster](gobuster_manual.md): Aplicación para realizar ataques de fuerza bruta contra URIs (directorios y archivos) y subdominios DNS.

[Nikto](nikto_manual.md): Escáner web de código abierto que realiza pruebas exhaustivas contra servidores web para detectar archivos peligrosos y software desactualizado.

[WPScan](wpscan_manual.md): Escáner de seguridad específico para WordPress.

🔐 4. Cracking de Contraseñas y Criptografía
Herramientas para recuperar o descifrar claves de acceso.

[John the Ripper](john_manual.md): Uno de los crackeadores de contraseñas más rápidos y versátiles, capaz de detectar automáticamente el tipo de hash.

Hashcat: Motor de recuperación de contraseñas basado en GPU, diseñado para ataques masivos de fuerza bruta y diccionarios.

[Hydra](hydra_manual.md): Herramienta de inicio de sesión por fuerza bruta en red muy rápida, compatible con protocolos como SSH, FTP, HTTP y más.

🚀 5. Explotación y Post-Explotación
Acciones para ganar acceso y mantener la persistencia en el sistema objetivo.

Metasploit Framework: Plataforma de pruebas de penetración que permite escribir, probar y ejecutar código de explotación contra máquinas remotas.

Searchsploit: Herramienta de línea de comandos para buscar exploits conocidos en la base de datos de Exploit-DB de forma offline.

BeEF (Browser Exploitation Framework): Se centra en el aprovechamiento de vulnerabilidades en los navegadores web para controlar equipos de usuarios finales.
