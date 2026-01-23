# 🕵️ Manual de Uso: WhatWeb

### 💻 Ejemplo de Uso Real

```bash
# Escaneo agresivo (nivel 3), detallado (verbose) y guardando log
whatweb -a 3 -v --log-json=resultado.json --proxy 127.0.0.1:8080 target.com
(sin argumentos) : Escaneo básico. Muestra una línea resumen con servidor, CMS y tecnologías.

-v : Modo Verbose. Muestra detalles completos y descripciones de cada plugin encontrado.

-a [1,3,4] : Nivel de Agresión. Define la intensidad del escaneo:

1 (Pasivo): Peticiones estándar HTTP.

3 (Agresivo): Intenta detectar versiones exactas de plugins.

4 (Pesado): Envía muchas peticiones (Ruidoso).

-i [archivo] : Escanea múltiples objetivos leyendo desde un archivo de texto.

--proxy [IP:Puerto] : Enruta el tráfico a través de un proxy (útil para Tor o Burp Suite).

--log-json=[archivo] : Guarda los resultados en formato JSON para análisis posterior o automatización.
