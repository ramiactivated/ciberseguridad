# 🏴‍☠️ Manual de Uso: John the Ripper

> Crackeador de contraseñas rápido y versátil (JtR).

### 💻 Ejemplo de Uso Real

```bash
# Ataque usando el diccionario 'RockYou' especificando el formato del hash
john --wordlist=/usr/share/wordlists/rockyou.txt --format=Raw-MD5 hash.txt

john [archivo] : Ejecución básica. Intenta crackear usando su modo por defecto (Single Crack + Wordlist interna).

--wordlist=[ruta] : Le indica a John que use un diccionario específico en lugar del predeterminado.

Ejemplo: rockyou.txt

--format=[tipo] : Especifica manualmente el tipo de hash (MD5, SHA256, NT, etc.). Ayuda cuando John no lo detecta automáticamente.

--show : Muestra en pantalla las contraseñas que ya han sido crackeadas anteriormente (lee del archivo john.pot).

unshadow [passwd] [shadow] : Comando auxiliar. Combina los archivos de sistema Linux (/etc/passwd y /etc/shadow) en un solo archivo de texto para poder atacarlos con John.
