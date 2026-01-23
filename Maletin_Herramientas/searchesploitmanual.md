# 🔦 Manual de Uso: Searchsploit

> Búsqueda offline en la base de datos masiva de Exploit-DB. Ideal para entornos aislados sin internet.

### 💻 Ejemplo de Uso Real

```bash
# 1. Buscar exploits para Windows y el servicio SMB
searchsploit windows smb

# 2. Copiar el exploit de interés (ID 42315) a tu carpeta actual para usarlo
searchsploit -m 42315

searchsploit [términos] : Búsqueda básica. Busca coincidencias en la base de datos local (ej: apache 2.4 o windows 10).

-m [ID] : Mirror (Copiar). Copia el archivo del exploit a tu directorio de trabajo actual.

Nota: Es más seguro que editar el original en la base de datos.

-x [ID] : Examinar. Abre el exploit en el editor de texto para leer el código o las instrucciones de uso.

-u : Update. Actualiza la base de datos local de Exploit-DB (requiere internet para este paso).
