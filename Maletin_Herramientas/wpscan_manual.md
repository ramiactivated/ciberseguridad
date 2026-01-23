# 🛡️ Manual de Uso: WPScan

> Escáner de seguridad de caja negra específico para instalaciones de WordPress.

### 💻 Ejemplo de Uso Real

```bash
# Enumeración de usuarios y plugins vulnerables usando API Token para ver los CVEs
wpscan --url [http://blog-objetivo.com](http://blog-objetivo.com) -e u,vp --api-token TU_TOKEN_AQUI --stealthy

--url : Define el Objetivo básico (la dirección del sitio WordPress).

-e u : Enumeración de Usuarios. Intenta extraer la lista de usuarios registrados (útil para atacar sus contraseñas después).

-e vp,vt : Busca específicamente Plugins Vulnerables (vp) y Temas Vulnerables (vt) en su base de datos.

-P [diccionario] : Lanza un ataque de fuerza bruta de contraseñas contra los usuarios detectados usando un archivo de claves.

--api-token : RECOMENDADO. Usa el token gratuito (de wpscan.com) para mostrar detalles técnicos y CVEs de las vulnerabilidades.

--stealthy : Modo Sigiloso. Intenta evadir sistemas de detección haciendo chequeos limitados y pasivos.
