# adaga.tech - Technical Portfolio

Portfolio web de una sola pagina enfocado en AI Systems, Computer Vision, NLP aplicado a NOM-035 y automatizacion tecnica.

## Estado actual

- Dominio activo esperado: `adaga.tech`.
- UI principal: `index.html` (Tailwind CDN + estilos embebidos).
- Navegacion SPA con anclas internas y `scroll-behavior: smooth`.
- Layout optimizado para desktop y mobile.

## Estructura del repositorio

- `index.html`: Sitio productivo publicado en GitHub Pages.
- `assets/projects/`: Evidencias visuales y CV PDF usado por la UI.
- `CNAME`: Dominio personalizado (`adaga.tech`).
- `archive/legacy/`: Archivos y versiones previas movidas fuera de produccion.

## Historial de implementacion

Se registro un resumen de cambios en:

- `docs/IMPLEMENTATION_LOG.md`

Incluye ajustes de contenido real, limpieza de placeholders, mejoras mobile, y organizacion del workspace.

## Mantenimiento rapido

1. Editar contenido visual y copy en `index.html`.
2. Agregar/reemplazar assets en `assets/projects/`.
3. Verificar rutas relativas de imagenes y PDF.
4. Hacer commit y push a `main` para desplegar.

## Preview local

En Windows PowerShell:

```powershell
py -m http.server 5500
```

Abrir:

- `http://127.0.0.1:5500/index.html`

## GitHub Pages y dominio

- Branch de despliegue: `main`.
- Carpeta de despliegue: `/ (root)`.
- Custom domain en Pages: `adaga.tech`.
- Mantener `CNAME` versionado en el repositorio.
