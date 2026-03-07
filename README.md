# adaga.tech - Portafolio I+D

Portafolio técnico para perfiles de Investigación y Desarrollo (I+D) en Ingeniería en Materiales y Automatización. Optimizado para reclutadores de Mitacs y DAAD.

## Estructura

- `index.html`: Marcado semántico y estructura de datos.
- `style.css`: Estilos "Dark Mode" tipo terminal industrial.
- Placeholders preparados para integraciones futuras de visualización de datos (Matplotlib, Plotly, D3.js).

## Despliegue en GitHub Pages con Dominio Personalizado (adaga.tech)

Para servir este portafolio bajo el dominio `adaga.tech`, sigue estos pasos exactos:

### 1. Preparación del Repositorio
1. Crea un repositorio en GitHub (ej. `adaga-portfolio`).
2. Sube los archivos `index.html`, `style.css` y este `README.md` a la rama `main` (o `master`).

### 2. Configuración en GitHub
1. Ve a los **Settings** de tu repositorio en GitHub.
2. Navega a la sección **Pages** (menú lateral izquierdo).
3. En **Source**, selecciona `Deploy from a branch`.
4. En **Branch**, selecciona `main` y la carpeta `/ (root)`. Guarda los cambios.
5. En la sección **Custom domain**, escribe `adaga.tech` y haz clic en **Save**. Esto generará automáticamente un archivo llamado `CNAME` en tu repositorio.

### 3. Configuración del Proveedor de Dominio (DNS)
Ingresa al panel de administración donde compraste `adaga.tech` (Namecheap, GoDaddy, Cloudflare, etc.) y configura los siguientes registros DNS:

**Registros A (A Records) apuntando a las IPs de GitHub:**
- Type: `A`, Host/Name: `@`, Value: `185.199.108.153`
- Type: `A`, Host/Name: `@`, Value: `185.199.109.153`
- Type: `A`, Host/Name: `@`, Value: `185.199.110.153`
- Type: `A`, Host/Name: `@`, Value: `185.199.111.153`

**Registro CNAME (Para el subdominio www):**
- Type: `CNAME`, Host/Name: `www`, Value: `TU_USUARIO.github.io` (reemplaza `TU_USUARIO` con tu nombre de usuario de GitHub).

### 4. Seguridad (HTTPS)
Regresa a GitHub Pages (*Settings > Pages*) y espera a que la propagación DNS termine (puede tardar desde 15 minutos hasta 24 horas). Una vez detectado, asegúrate de marcar la casilla **"Enforce HTTPS"**.
