# Infraestructura

Este repositorio centraliza el despliegue de toda la aplicación.

## 1. Estructura de Carpetas Obligatoria

Para que el sistema funcione, se deben tener los repositorios al mismo nivel dentro de una carpeta raíz **Los nombres de las carpetas deben estar estrictamente en minúscula**:

```text
raiz/
├── backend/           
├── frontend-web/       
├── frontend-movil/     
└── infraestructura/    
```

## 2. Configuración (`.env`)

1. Entra en `infraestructura/`.
2. Crea una copia de `.env.examples` llamada `.env`. (**Nunca se sube el .env al repositorio**)
3. Edita `.env` y configura la URL de Neon correcta.


## 3. Ejecución con Docker

Desde la carpeta `infraestructura/`:

### Levantar el proyecto completo:

Desde la carpeta `infraestructura/`, ejecuta:

| Acción | Comando |
| --- | --- |
| **Arrancar todo** | `docker compose up --build` |
| **Segundo plano** | `docker compose up -d` |
| **Ver estado** | `docker compose ps` |
| **Parar todo** | `docker compose down` |

## 4. Github
Ver las normas completas en [GITHUB.md](./GITHUB.md)