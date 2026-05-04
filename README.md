# 🚀 Diego — Portfolio Personal

Portafolio personal construido con **Astro 4**, CSS moderno y sin dependencias de UI externas.

## Stack
- **Framework**: Astro 4
- **Estilos**: CSS puro con custom properties (sin Tailwind, para aprender CSS real)
- **Scripts**: TypeScript nativo de Astro
- **Fuentes**: Syne + DM Sans (Google Fonts)

## Estructura del proyecto

```
portfolio/
├── src/
│   ├── components/       ← Cada sección es un componente .astro
│   │   ├── Nav.astro
│   │   ├── Hero.astro
│   │   ├── About.astro
│   │   ├── Projects.astro
│   │   ├── Experience.astro
│   │   └── Footer.astro
│   ├── layouts/
│   │   └── Layout.astro  ← Shell HTML (head, body, fuentes)
│   ├── pages/
│   │   └── index.astro   ← Ruta "/" — ensambla todo
│   └── styles/
│       └── global.css    ← Design tokens y utilidades globales
├── public/
│   └── cv-diego.pdf      ← (Coloca tu CV aquí)
├── astro.config.mjs
└── package.json
```

## Cómo correrlo localmente

```bash
# 1. Instala dependencias
npm install

# 2. Servidor de desarrollo con hot-reload
npm run dev
# → Abre http://localhost:4321

# 3. Build para producción
npm run build

# 4. Preview del build
npm run preview
```

## Personalización — qué cambiar

| Archivo | Qué actualizar |
|---------|---------------|
| `Hero.astro` | Tu nombre, descripción, roles |
| `About.astro` | Skills y porcentajes, certificaciones |
| `Projects.astro` | Tus proyectos, URLs de GitHub y demo |
| `Experience.astro` | Empresa real, fechas, educación |
| `Footer.astro` | URLs de redes sociales y email |
| `public/cv-diego.pdf` | Tu CV en PDF para descargar |

## Deploy gratuito recomendado

```bash
# Vercel (más fácil)
npm i -g vercel
vercel

# Netlify
npm run build
# → sube la carpeta dist/ a netlify.com/drop
```

## Conceptos de Astro que aprendes en este proyecto

1. **Componentes .astro**: frontmatter (servidor) + template HTML + `<style>` scoped
2. **Layouts**: el "shell" que envuelve páginas con `<slot />`
3. **Pages**: cada `.astro` en `src/pages/` = una ruta URL
4. **Props**: `interface Props` + `Astro.props` para datos externos
5. **Scoped styles**: los `<style>` aplican SOLO al componente actual
6. **Client scripts**: `<script>` para lógica que corre en el browser
7. **Static site generation**: todo se pre-renderiza en build time (0 JS por defecto)
