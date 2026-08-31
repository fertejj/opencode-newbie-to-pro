# OpenCode Pro Roadmap

Hoja de ruta visual y estática para aprender OpenCode, creada con Astro.

## Uso

```bash
npm install
npm run dev
```

Para crear los archivos estáticos de publicación:

```bash
npm run build
```

El resultado se genera en `dist/`. Es un sitio estático: puede publicarse en un hosting de estáticos y usar Cloudinary para imágenes, vídeos u otros assets optimizados.

## Publicación automática en Cloudflare Pages

El repositorio incluye un workflow de GitHub Actions. Cuando agregues los dos secretos indicados abajo, cada `push` a `main` construirá el sitio y lo publicará en el proyecto Pages `opencode-newbie-to-pro`.

1. En Cloudflare, crea un token con permiso **Account → Cloudflare Pages → Edit**.
2. Copia tu **Account ID** desde el panel de Cloudflare.
3. En GitHub, abre `fertejj/opencode-newbie-to-pro` → **Settings** → **Secrets and variables** → **Actions** → **New repository secret**.
4. Agrega estos secretos (no los publiques ni los compartas):
   - `CLOUDFLARE_API_TOKEN`
   - `CLOUDFLARE_ACCOUNT_ID`
5. En GitHub, abre **Actions** y ejecuta el workflow **Deploy to Cloudflare Pages** una vez. Ese primer despliegue creará el proyecto Pages si todavía no existe.

Al finalizar, el proyecto tendrá una URL similar a `opencode-newbie-to-pro.pages.dev`. Desde Pages podrás asociar `opencode-guide.fertejj.com`; en DonWeb crearás el CNAME que Pages indique para ese subdominio.
