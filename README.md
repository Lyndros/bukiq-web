# Bukiq — Landing Page

Landing page de [Bukiq](https://bukiq.com), plataforma de gestión de reservas para restaurantes con asistente de voz 24/7.

## Stack

- **[Astro](https://astro.build/)** v6 — framework de generación estática
- **[Tailwind CSS](https://tailwindcss.com/)** v3 — utilidades CSS
- **[@tailwindcss/typography](https://tailwindcss.com/docs/typography-plugin)** — tipografía para páginas legales

## Inicio rápido

```bash
npm install
npm run dev       # http://localhost:4321
```

### Otros comandos

| Comando           | Descripción                                  |
| ----------------- | -------------------------------------------- |
| `npm run dev`     | Servidor de desarrollo con HMR               |
| `npm run build`   | Genera el sitio estático en `dist/`          |
| `npm run preview` | Previsualiza el build de producción          |

## Estructura del proyecto

```
bukiq-web/
├── public/
│   ├── bukiq-logo.svg          # Logo horizontal
│   ├── bukiq-logov.svg         # Logo vertical
│   ├── favicon.svg             # Favicon (icono del teléfono)
│   └── images/                 # Avatares para testimonios
│       ├── avatar-marta.jpg
│       ├── avatar-carlos.jpg
│       └── avatar-laura.jpg
├── src/
│   ├── layouts/
│   │   ├── MainLayout.astro    # Layout principal (SEO, fuentes, estilos globales)
│   │   └── LegalLayout.astro   # Layout para páginas legales (prose, navegación)
│   ├── pages/
│   │   ├── index.astro         # Landing page principal
│   │   ├── aviso-legal.astro   # Aviso legal (LSSI-CE)
│   │   ├── privacidad.astro    # Política de privacidad (RGPD/LOPDGDD)
│   │   ├── cookies.astro       # Política de cookies
│   │   └── terminos.astro      # Términos del servicio
│   └── components/
│       ├── Header.astro        # Cabecera sticky con logo y navegación
│       ├── Hero.astro          # Sección principal con CTA y mockup del panel
│       ├── ProblemSolution.astro
│       ├── Features.astro      # Grid de 6 funcionalidades
│       ├── HowItWorks.astro    # 3 pasos del flujo de uso
│       ├── DashboardPreview.astro
│       ├── Benefits.astro
│       ├── Testimonials.astro
│       ├── FAQ.astro           # Acordeón con <details>/<summary>
│       ├── CTA.astro           # Llamada a la acción final
│       └── Footer.astro        # Pie con logo, email y enlaces legales
├── astro.config.mjs
├── tailwind.config.mjs
└── tsconfig.json
```

## Colores de marca

| Token   | Hex       | Uso                          |
| ------- | --------- | ---------------------------- |
| `azul`  | `#223C78` | Color principal (corporativo)|
| `verde` | `#7AC034` | Color de acento              |

Definidos en `tailwind.config.mjs` y utilizables como `text-azul`, `bg-verde`, etc.

## Páginas legales

Las cuatro páginas requeridas por la legislación española están implementadas:

| Página               | Ruta             | Normativa         |
| -------------------- | ---------------- | ----------------- |
| Aviso legal          | `/aviso-legal`   | LSSI-CE           |
| Política de privacidad | `/privacidad`  | RGPD / LOPDGDD    |
| Política de cookies  | `/cookies`       | LSSI-CE / RGPD    |
| Términos del servicio | `/terminos`     | —                 |

> **Nota:** El NIF/CIF y domicilio en el aviso legal están marcados como `[pendiente de completar]`.

## Enlaces externos

- **Demo:** todos los botones "Solicitar demo" enlazan a [cal.eu/bukiq/30min](https://cal.eu/bukiq/30min)
- **Contacto:** [hola@bukiq.com](mailto:hola@bukiq.com)

## Despliegue

El sitio es completamente estático. Tras ejecutar `npm run build`, el contenido de `dist/` se puede servir desde cualquier CDN o hosting estático (Vercel, Netlify, Cloudflare Pages, GitHub Pages, etc.).

## Licencia

Todos los derechos reservados. © Bukiq.
