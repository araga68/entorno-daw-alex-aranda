# Documentación de mi entorno de desarrollo · Práctica 2

**Alejandro Aranda Aguilar:**
**URL de mi repositorio:**

> Rellena cada apartado a medida que avanzas. Donde pone «pega aquí», copia el texto
> de la terminal (no hace falta captura). Escribe con tus palabras: no se valora la longitud,
> sino que se note que entiendes lo que has hecho.

---

## 1. Instalación de entornos (CE 2.a)

### 1.1. Entorno vacío (paso 3)

Resultado de `java -version` y `node -v` **antes** de instalar nada:

```
openjdk version "27" 2026-09-15
OpenJDK Runtime Environment Temurin-27+35 (build 27+35)
OpenJDK 64-Bit Server VM Temurin-27+35 (build 27+35, mixed mode, sharing)
```

¿Por qué crees que aparece ese mensaje? (relaciónalo con la diapositiva «Problemas habituales del entorno»)

> 

### 1.2. Después de la 1.ª reconstrucción (paso 5)

Resultado de `java -version`, `node -v` y `jupyter lab --version` **después**:

```
v24.22.1
4.6.4
```

¿Qué líneas nuevas han aparecido en `devcontainer.json`? Explica con tus palabras qué hace cada una:

>  "ghcr.io/devcontainers/features/java:1": {},
    "ghcr.io/devcontainers/features/node:2": {},

    Instala Java en el contenedor para poder ejecutar programas Java y utilizar herramientas de desarrollo relacionadas y instala Node, que permite ejecutar JavaScript fuera del navegador y utilizar herramientas como npm para gestionar paquetes.

### 1.3. Comparativa de los dos IDE (paso 6)

|                                         | Editor de GitHub Codespaces | JupyterLab |
|-----------------------------------------|-----------------------------|------------|
| ¿Libre o propietario?                   |                        github es propietario y JupyterLab libre.

| Licencia / empresa o comunidad          |                             |       github es empresa (Microsoft) y JupyterLab comunidad.   
| ¿Tiene coste? ¿Con qué límites?         |                             |         La diferencia principal es que GitHub Codespaces cobra por los recursos que utilizas, mientras que JupyterLab es gratuito como software, aunque el servidor donde lo ejecutes puede tener un coste.

| ¿Se puede usar fuera de GitHub?         |                             |          GitHub Codespaces no como servicio independiente y jupiterLab si.

| Lo que más me ha gustado                |                             |            |
| Lo que menos me ha gustado              |                             |            |
| ¿Para qué tipo de trabajo lo elegiría?  |                             |            |
Para desarrollar aplicaciones web, Java o Node.js en un entorno en la nube.
---

## 2. Módulos y extensiones (CE 2.b)

| Extensión | ¿Para qué sirve? | ¿Qué cambió al instalarla? | ¿La mantengo? ¿Por qué? |
|-----------|------------------|----------------------------|-------------------------|
| Extension Pack for Java |   |   |   |
| Code Spell Checker      |   |   |   |

¿Qué diferencia hay entre instalar una extensión **solo desde el panel** y añadirla **también a `devcontainer.json`**?

> Instalar una extensión solo desde el panel de Visual Studio Code: se instala manualmente en tu entorno actual. Si creas otro contenedor o Codespace, puede que tengas que instalarla de nuevo.

Añadirla también a devcontainer.json: la instalación queda declarada en la configuración del proyecto y se instala automáticamente al crear el entorno de desarrollo.

---

## 3. Personalización y automatización (CE 2.c)

- **Tema visual elegido** (paso 10) y por qué:
- **Ajuste del proyecto** (paso 10). ¿Qué archivo se ha creado y qué contiene?

```
pega aquí el contenido de .vscode/settings.json
```

- **Atajo de teclado** (paso 11). ¿Qué acción, qué combinación y para qué te sirve?
- **Snippet** (paso 12). ¿Qué escribes y qué aparece?
- **Automatización al crear el entorno** (paso 14). ¿Qué hace `postCreateCommand` y qué archivos/carpetas han aparecido después de reconstruir?
- **Tareas** (paso 13). ¿Cuántas tareas hay en `tasks.json` y qué hace cada una?

¿Qué parte de toda esta configuración es **personal** (solo para ti) y qué parte es **del proyecto** (la recibe cualquiera que abra el repositorio)?

> 

---

## 4. Ejecutables de diferentes lenguajes en el mismo entorno (CE 2.e)

Salida completa de la tarea **Build completo** (paso 15):

```
=== FACTURA generada con Java 25.0.4.1 ===
Dominio web anual              12.00 EUR
Alojamiento web                59.90 EUR
Logotipo corporativo          150.00 EUR
-----------------------------------------
Base imponible                221.90 EUR
IVA (21 %)                     46.60 EUR
TOTAL                         268.50 EUR
```

| Lenguaje | Archivo fuente | Herramienta que lo traduce | Archivo generado | Cómo se ejecuta |
|----------|----------------|----------------------------|------------------|-----------------|
| Java       | `src/java/Factura.java` |   |   |   |
| TypeScript | `src/ts/factura.ts`     |   |   |   |

**Opcional:** ¿has podido ejecutar los mismos archivos desde JupyterLab (paso 19)? ¿Por qué funciona en los dos IDE sin instalar nada más?

> 

---

## 5. Sistema de actualizaciones (CE 2.d)

| Elemento | ¿Quién lo actualiza? | Modo (automático / manual / ninguno) | Qué he configurado yo |
|----------|----------------------|--------------------------------------|-----------------------|
| El editor de Codespaces |   |   |   |
| Las extensiones         |   |   |   |
| Java                    |   |   |   |
| Node.js                 |   |   |   |
| Dependencias npm (lodash, typescript…) |   |   |   |

Versión de Java **antes** (paso 5) y **después** (paso 18):

```
pega aquí
```

Resultado de `npm outdated` (paso 17):

```
     Depended by
@types/lodash  4.14.202  4.14.202  4.17.27  node_modules/@types/lodash  entorno-daw-alex-aranda
@types/node    20.11.30  20.11.30   26.6.5  node_modules/@types/node    entorno-daw-alex-aranda
lodash          4.17.20   4.17.20   4.18.1  node_modules/lodash         entorno-daw-alex-aranda
typescript        5.4.5     5.4.5    7.0.2  node_modules/typescript     entorno-daw-alex-aranda
```

Resultado de `npm audit` **antes** de actualizar lodash (solo el resumen final):

```
pega aquí
```

Resultado de `npm audit` **después**:

```
it` functions - https://github.com/advisories/GHSA-xxjr-mmjv-4gpg
fix available via `npm audit fix --force`
Will install lodash@4.18.1, which is outside the stated dependency range
node_modules/lodash

1 high severity vulnerability

To address all issues, run:
  npm audit fix --force
```

**Mi política de actualizaciones**: si este entorno lo usara un equipo de 5 personas durante todo el curso, ¿qué dejarías en automático y qué fijarías a mano? Justifícalo.

> 

---

## 6. Incidencias

Anota cualquier problema que hayas tenido y cómo lo resolviste (también si usaste un fragmento completo).

> 

## 7. Reflexión final

¿Qué ventaja tiene describir el entorno «como código» frente a instalar cada programa a mano en tu ordenador? Piensa en un equipo con Mac y Windows.

> La ventaja es que todos tenemos el mismo entorno de desarrollo, aunque usemos Mac o Windows, sin tener que instalar los programas uno por uno. Así ahorramos tiempo y evitamos problemas de compatibilidad.
