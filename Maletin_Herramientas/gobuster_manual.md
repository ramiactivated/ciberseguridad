# 👻 Manual de Uso: Gobuster

> Herramienta de fuerza bruta para descubrir directorios, archivos y subdominios ocultos.

### 💻 Ejemplo de Uso Real

```bash
# Búsqueda de directorios y archivos (php, html) con 50 hilos de velocidad
gobuster dir -u [http://target.com](http://target.com) -w /usr/share/wordlists/dirb/common.txt -x php,html,txt -t 50 -o resultado.txt

dir : Activa el Modo de enumeración. Busca directorios y archivos en la web.

-u <URL> : Especifica la URL del objetivo (debe incluir http:// o https://).

-w <wordlist> : Ruta al diccionario de palabras que se usará para la fuerza bruta.

-x php,html,txt : Añade extensiones de archivo a las palabras del diccionario para encontrar archivos específicos.

-t 50 : Aumenta el número de hilos (threads) a 50 para mayor velocidad (por defecto es 10).

-o resultado.txt : Guarda los hallazgos positivos en un archivo para consultarlos luego.
