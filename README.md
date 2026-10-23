# Hoja de vida tecnológica — Julian Felipe Moreno

Tarjeta de presentación digital en formato web: HTML, CSS y JavaScript puros, sin
dependencias ni build step. Pensada para desplegarse directamente en **Vercel**.

## Estructura del proyecto

```
julian-cv-web/
├── index.html     → contenido y estructura
├── styles.css     → diseño visual (tema claro/oscuro incluido)
├── script.js      → menú móvil, scroll, tema, copiar contacto
└── README.md
```

## Ver el sitio en tu computador

No necesitas instalar nada: puedes abrir `index.html` directamente en el navegador.
Para una vista más fiel (recomendado, por las rutas de las fuentes), puedes usar un
servidor local simple:

```bash
npx serve .
```

y abrir la URL que te indique en la terminal (normalmente `http://localhost:3000`).

## Desplegar en Vercel

### Opción 1 — Desde la web de Vercel (sin usar la terminal)

1. Sube esta carpeta a un repositorio en GitHub (puedes crear uno nuevo, por ejemplo
   `julian-cv-web`, y subir estos archivos).
2. Entra a [vercel.com](https://vercel.com) e inicia sesión con tu cuenta de GitHub.
3. Clic en **Add New → Project**, selecciona el repositorio y confirma.
4. Como es un sitio estático, Vercel lo detecta automáticamente (no necesitas
   configurar "Build Command" ni "Output Directory" — déjalos vacíos o en
   "Other").
5. Clic en **Deploy**. En menos de un minuto tendrás una URL tipo
   `https://julian-cv-web.vercel.app`.

### Opción 2 — Con la CLI de Vercel (más rápido si ya usas terminal)

```bash
npm i -g vercel
cd julian-cv-web
vercel login
vercel --prod
```

La CLI te dará una URL pública al finalizar.

### Dominio propio (opcional)

Desde el panel del proyecto en Vercel: **Settings → Domains**, puedes conectar un
dominio propio (por ejemplo `julianmoreno.dev`) si decides comprar uno.

## Personalización recomendada antes de publicar

- Revisa las fechas de la experiencia en **EFP Consulting S.A.S.**: en tu CV figura
  "Ene 2025 – Jun 2026", pero la certificación laboral adjunta indica
  "Ene 2024 – Jul 2026". Te dejé el dato tal como aparece en tu CV principal;
  confírmalo y ajústalo en `index.html` si es necesario.
- Si más adelante quieres mostrar proyectos reales (repos de GitHub, capturas,
  demos), se puede agregar fácilmente una sección "Proyectos" — dime cuáles y los
  integro.
- Por seguridad, este sitio **no incluye tu número de cédula ni los certificados
  laborales adjuntos al PDF original** — esa información no debería publicarse en
  una página web pública.
- Si quieres un botón de "Descargar CV en PDF", genera una versión limpia (sin los
  certificados ni datos sensibles) y colócala como `assets/CV-Julian-Moreno.pdf`;
  puedo ayudarte a generar ese PDF si lo necesitas.
- El logo/favicon actual es un monograma "JM" generado por código. Si tienes una
  foto profesional o un logo personal, se puede reemplazar fácilmente.

## Edición de contenido

Todo el texto vive en `index.html`, organizado por secciones (`id="perfil"`,
`id="experiencia"`, `id="habilidades"`, `id="estudios"`, `id="contacto"`). Los
colores y tipografía se controlan desde las variables en la parte superior de
`styles.css` (`:root { ... }`).
