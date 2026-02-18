# Normas de Trabajo en GitHub

## Reglas
* Prohibido subir el archivo `.env`
* No se deben subir carpetas `.venv/`, `__pycache__/`, binarios, compilados o archivos temporales de editores.
* Antes de hacer un `push`, revisa qué estás enviando:
1. **Terminal**: `git status`
2. **GUI**: Revisa la lista de archivos en GitHub Desktop o VS Code.


## 2. Estrategia de Ramas

Utilizaremos dos ramas remotas principales y, opcionalmente, ramas locales para tareas específicas:

| Rama | Propósito | 
| --- | --- |
| `main` | **Producción / Hitos**: Solo contiene versiones terminadas (Hitos u otras fechas señaladas). | 
| `develop` | **Integración**: Rama principal de trabajo diario. Aquí se une el código de todos. | 
| `feature/` (opcional) | **Tareas locales**: Ramas temporales para desarrollar funcionalidades o cambios sin afectar `develop`. Ej: `feature/login`. |

El código desarrollado se sube a develop, y solo cuando el proyecto es estable, se pasa a main

> **Uso de `feature/` opcional:**
>
> 1. Crear rama local `feature/*` para trabajar sin tocar `develop`.
> 2. Hacer commits atómicos y claros en la rama `feature`.
> 3. Cuando esté listo, mergear localmente los cambios en `develop`.
> 4. Solo `develop` y `main` existen en el remoto; las ramas `feature/` pueden quedarse locales.


## 3. Sincronización Diaria (Obligatorio)

Para evitar los conflictos de código, sigue estos pasos **antes de empezar a programar**:

1. **Sincroniza la Infraestructura**: `git pull` en el repo de `infraestructura`.
2. **Sincroniza tu Repo**: `git pull` en el repositorio en el que vayas a trabajar.

> **¿Hay conflictos?** Mantén la calma. Usa Visual Studio Code para comparar las versiones. Si no estás seguro de qué borrar, consulta con el compañero que tocó esa parte antes de aceptar los cambios.

## 4. Convención de Commits (Opcional)

Usaremos **Conventional Commits** para que el historial sea legible. El formato es: `tipo: descripción corta en minúsculas`.

### Tipos Permitidos:

| Tipo | Cuándo usarlo | Ejemplo |
| --- | --- | --- |
| **feat** | Nueva funcionalidad o lógica de juego. | `feat: añadir sistema de combate` |
| **fix** | Corrección de un error o bug. | `fix: corregir timeout en neon` |
| **docs** | Cambios en documentación o READMEs. | `docs: actualizar guía de instalación` |
| **style** | Formato, espacios, CSS (sin tocar lógica). | `style: corregir indentación` |
| **refactor** | Mejora de código (no añade función ni arregla bug). | `refactor: optimizar bucle de mapa` |
| **chore** | Tareas de mantenimiento o herramientas. | `chore: actualizar .gitignore` |

---

## 5. Consejos para un flujo fluido

* **Commits Recurrentes**: No esperes a terminar muchas cosas para hacer el commit. Ves guardando versiones conforme logras cambios significativos.
* **Mensajes Claros**: Evita mensajes como "cambios", "update" o "arreglado". Sé específico.
* **Atomicidad**: Intenta que cada commit haga una sola cosa. Si arreglas un bug y añades una función, haz dos commits.