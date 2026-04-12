# 🌍 planetaalofoke.online

🔗 **[https://planetaalofoke.online](https://planetaalofoke.online)**

Sitio web de fans no oficial para **Planeta Alofoke 2026**, el reality show digital más grande de República Dominicana producido por Santiago Matías "Alofoke" y Alofoke Media Group.

---

## Stack Técnico

- **Frontend:** HTML5, CSS3, JavaScript vanilla — sin frameworks
- **Servidor:** VPS Contabo (Ubuntu 24) con Nginx + SSL Let's Encrypt
- **Dominio:** GoDaddy → `planetaalofoke.online`
- **Hosting de video:** YouTube embed (canal oficial `@alofokeradioshow`)

---

## Estructura del Proyecto

```
/
├── index.html                        # Home — live embed + participantes + chismes + FAQ
├── participantes.html                # Grid de los 15 participantes con fotos y status
├── como-ver.html                     # Guía para ver desde cualquier país
├── privacidad.html                   # Política de privacidad (requerida para AdSense)
├── sitemap.xml                       # News Sitemap con hreflang y 16 URLs
├── robots.txt
├── favicon.svg
├── og-image.jpg
├── site.webmanifest
├── img/                              # Fotos 400x400 JPG de los 15 participantes
├── blog/
│   ├── index.html
│   ├── participantes-confirmados.html
│   ├── alofoke-en-vivo.html
│   ├── santiago-matias-alofoke.html
│   ├── alofoke-se-va-de-univision.html
│   ├── que-es-planeta-alofoke.html
│   ├── como-votar.html
│   ├── historia-alofoke.html
│   └── youtube-alofoke.html
└── chismes/
    ├── index.html
    ├── ana-beato-brayan-elton.html
    ├── karla-alvarez-jet-set.html
    └── pamela-infante-wander-franco.html
```

---

## Participantes (15 Confirmados)

| Nombre | Instagram |
|--------|-----------|
| Karla Alvarez | @kaarllitaa_ |
| Natalia Salas | @nataliasalasvv |
| Pamela Infante | @infante_095 |
| Bibi Corena | @bibioficial_7 |
| Liguita Teteo | @liguitateteo |
| Hillary Rachel | @hillaryrguerrero |
| La Mas Doll | @soylamasdoll |
| La Fruta | @lafruta_oficial |
| Nacho Estrella | @nachoestrella1 |
| Sammy Greatest | @sammygreatest |
| Ana Beato | @ana.beato |
| Aldo Farías | @aldofariasrd |
| Laura Sahar | @laurasahar00 |
| Messiah | @messiahgram |
| Etervidos | @etervidos |

---

## SEO Implementado

### Datos Estructurados (Schema JSON-LD)
- `Organization` + `WebSite` + `WebPage` + `BreadcrumbList`
- `Event` — Grand Premiere Live
- `HowTo` — Cómo ver Planeta Alofoke
- `FAQPage` — 6 preguntas frecuentes
- `VideoObject` — embed de YouTube
- `Speakable` — Google Assistant / voice search
- `Article` + `BlogPosting` — artículos del blog
- `Person` — participantes

### Keywords Objetivo
- `planeta alofoke participantes` — posición principal
- `planeta alofoke en vivo` — keyword de alto volumen post-estreno
- `ver planeta alofoke gratis` — intent transaccional
- `planeta alofoke 2026` — keyword evergreen
- Nombres individuales de cada participante

### Hreflang
Implementado en todas las páginas: `es`, `es-419`, `es-US`, `es-ES`, `x-default`

### News Sitemap
Todas las páginas de blog y chismes incluidas con `<news:news>` para cobertura en Google News.

### Optimizaciones Técnicas
- `font-display: swap` en Google Fonts
- `loading="lazy"` en todas las imágenes
- `preconnect` a YouTube, Google Fonts y AdSense
- `fetchpriority="low"` en el iframe de YouTube
- Imágenes comprimidas a 400×400 JPG (~30-50KB)

---

## Monetización

- **Google AdSense** — pendiente de aplicar (target: 20 de abril, post-tráfico)
- **RPM estimado:** $0.30–0.80 RD / $2–5 USA
- Política de privacidad publicada en `/privacidad.html`

---

## Métricas Iniciales (Search Console — Primeros días)

| Métrica | Valor |
|---------|-------|
| Clicks (24h pico) | 45 |
| Impresiones (24h) | 398 |
| CTR | 11.3% |
| Posición media | 6.3 |
| Países | RD 83%, USA 17%, ES, VE, CO |
| Keywords rankeando | 27+ |

---

## Objetivo del Proyecto

Este proyecto fue desarrollado con el fin de **poner en práctica habilidades de desarrollo web y experimentar con el posicionamiento orgánico (SEO) de una página desde cero**. El contexto del reality show Planeta Alofoke 2026 fue elegido deliberadamente por su potencial de tráfico viral en el mercado hispanohablante — especialmente República Dominicana y Estados Unidos — en torno al estreno del 13 de abril de 2026.

El reto principal fue construir un sitio capaz de competir en Google en tiempo real, ajustando el contenido, los datos estructurados y las keywords a medida que el panorama del show evolucionaba. Esto permitió aprender de forma práctica sobre:

- Indexación y crawling en Google Search Console
- Implementación de Schema.org y News Sitemaps
- CTR y posicionamiento orgánico sin paid ads
- Creación de contenido SEO-first en español
- Optimización técnica de performance en servidor VPS con Nginx

> Sitio de fans no oficial. El contenido audiovisual es propiedad de Alofoke Media Group.

---

*Desarrollado por Julio Cesar Marte Sosa · Santo Domingo, República Dominicana · 2026*
