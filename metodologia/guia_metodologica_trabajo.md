📑 Metodología de un Pentesting (Paso a Paso)
Esta guía describe el ciclo de vida estándar de una prueba de penetración, desde el contacto inicial hasta el informe final.

1. Reconocimiento 
Es la fase de recolección de información. El objetivo es conocer el "perfil" del objetivo tanto como sea posible.

Pasivo (OSINT): Sin interactuar con el objetivo (Google Dorking, Whois, redes sociales).

Activo: Interactuando directamente.

Herramientas en tu maletín: theHarvester, WhatWeb.

2. Escaneo y Enumeración
Aquí buscamos puertas de entrada. Identificamos qué sistemas ahi, qué puertos tienen abiertos y qué servicios están corriendo (versiones exactas).

Objetivo: Identificar la superficie de ataque.

Acciones: Escaneo de puertos, enumeración de subdominios, descubrimiento de directorios ocultos.

Herramientas en tu maletín: Nmap, Gobuster.

3. Análisis de Vulnerabilidades
Con la información de la fase anterior, buscamos debilidades en los servicios detectados.

Acciones: Buscar versiones de software desactualizadas con exploits conocidos o fallos de configuración.

Herramientas en tu maletín: Nikto, WPScan, Searchsploit.

4. Explotación 
Es el momento de "entrar". Intentamos aprovechar las vulnerabilidades encontradas para ganar acceso al sistema.

Acciones: Lanzar exploits, realizar ataques de inyección SQL o fuerza bruta de contraseñas.

Objetivo: Obtener una "shell" o acceso inicial.

Herramientas en tu maletín: Metasploit, SQLmap, Hydra.

5. Post-Explotación 
Una vez dentro, el trabajo no ha terminado. Debemos ver qué tan profundo podemos llegar.

Escalada de Privilegios: Intentar pasar de un usuario normal a root o Administrator.

Movimiento Lateral: Saltas de una máquina a otra dentro de la red.

Persistencia: Configurar una forma de volver a entrar si nos cierran la conexión.

Herramientas en tu maletín: BeEF, Scripts de enumeración local.

6. Informe 
La fase más importante para un profesional.

Limpieza: Borrar archivos subidos, eliminar usuarios creados y cerrar backdoors. ¡No dejes rastro!

Informe: Documentar qué vulnerabilidades se encontraron, cómo se explotaron (con capturas) y, sobre todo, cómo arreglarlas.
