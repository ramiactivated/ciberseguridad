# 📑 Metodología de Pentesting (Paso a Paso)

> **Ciclo de vida estándar** de una prueba de penetración, desde el contacto inicial hasta el informe final.

---

## 📊 Flujo de Trabajo

```mermaid
graph TD
    A[1. Reconocimiento] --> B[2. Escaneo y Enum]
    B --> C[3. Análisis Vulns]
    C --> D[4. Explotación]
    D --> E[5. Post-Explotación]
    E --> F[6. Informe y Limpieza]
    
    style A fill:#f9f,stroke:#333,stroke-width:2px
    style D fill:#bbf,stroke:#333,stroke-width:2px
    style F fill:#bfb,stroke:#333,stroke-width:2px
```
# 📑 Metodología de Pentesting (Paso a Paso)

Esta guía describe el ciclo de vida estándar de una prueba de penetración, desde el contacto inicial hasta el informe final.

---

## 🕵️ 1. Reconocimiento
*La fase de recolección de información.*

El objetivo es conocer el "perfil" del objetivo tanto como sea posible antes de tocar nada.

* **Pasivo (OSINT):** Sin interactuar con el objetivo (Google Dorking, Whois, redes sociales).
* **Activo:** Interactuando directamente con la infraestructura.

> **🧰 Herramientas en tu maletín:**
> * [**theHarvester**](...Maletin_Herramientas/theHarvester_manual.md)
> * [**WhatWeb**](../whatweb_manual.md)
> * [**Shodan**](../README.md#%F0%9F%94%8D-1-reconocimiento-y-osint)

---

## 📡 2. Escaneo y Enumeración
*Buscando puertas de entrada.*

Identificamos qué sistemas hay, qué puertos tienen abiertos y qué servicios están corriendo (versiones exactas).

* **Objetivo:** Identificar la superficie de ataque completa.
* **Acciones:** Escaneo de puertos, enumeración de subdominios, descubrimiento de directorios ocultos.

> **🧰 Herramientas en tu maletín:**
> * [**Nmap**](../nmap_manual.md)
> * [**Gobuster**](../gobuster_manual.md)

---

## 🔬 3. Análisis de Vulnerabilidades
*Detectando fallos de seguridad.*

Con la información de la fase anterior, buscamos debilidades específicas en los servicios detectados.

* **Acciones:** Buscar versiones de software desactualizadas con exploits conocidos (CVEs) o fallos de configuración por defecto.

> **🧰 Herramientas en tu maletín:**
> * [**Nikto**](../nikto_manual.md)
> * [**WPScan**](../wpscan_manual.md)
> * [**Searchsploit**](../searchesploitmanual.md)

---

## 💥 4. Explotación
*El momento de "entrar".*

Intentamos aprovechar las vulnerabilidades encontradas para ganar acceso no autorizado al sistema.

* **Objetivo:** Obtener una "shell" (consola de comandos) o acceso inicial.
* **Acciones:** Lanzar exploits, realizar ataques de inyección SQL o fuerza bruta de contraseñas.

> **🧰 Herramientas en tu maletín:**
> * [**Metasploit**](../metamanual.md)
> * [**SQLmap**](../sqlmap_manual.md)
> * [**Hydra**](../hydra_manual.md)

---

## 🚩 5. Post-Explotación
*Una vez dentro, el trabajo no ha terminado.*

Debemos evaluar el impacto real del compromiso y ver qué tan profundo podemos llegar.

* **Escalada de Privilegios:** Intentar pasar de un usuario normal a `root` o `Administrator`.
* **Movimiento Lateral:** Saltar de una máquina a otra dentro de la red corporativa.
* **Persistencia:** Configurar una forma de volver a entrar si nos cierran la conexión (Backdoors).

> **🧰 Herramientas en tu maletín:**
> * [**BeEF**](../BeEFmanual.md)
> * [**John the Ripper**](../john_manual.md) *(Para crackear hashes obtenidos)*

---

## 📝 6. Informe y Limpieza
*La fase más importante para un profesional.*

> [!CAUTION]
> **Limpieza Obligatoria:** Debes borrar archivos subidos, eliminar usuarios creados y cerrar cualquier backdoor. **¡No dejes rastro!**

* **Informe Ejecutivo:** Resumen para la directiva (enfocado en el impacto de negocio).
* **Informe Técnico:** Documentar qué vulnerabilidades se encontraron, cómo se explotaron (con capturas de pantalla) y, sobre todo, **cómo arreglarlas (Remediación)**.
