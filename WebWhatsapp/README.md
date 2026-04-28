# WaTools 🟢 NO DISPONIBLE 

**Plataforma de herramientas gratuitas para WhatsApp**  
🌐 [watools.online](https://watools.online)

---

## ¿Qué es WaTools?

WaTools es un sitio web estático de herramientas gratuitas enfocadas en WhatsApp, orientado a monetización pasiva mediante tráfico SEO orgánico en español y Google AdSense. No tiene backend, no tiene base de datos, no tiene registro de usuarios.

---

## Herramientas

### 1. Convertidor de Audio WhatsApp → MP3
**URL:** `/index.html`

Convierte archivos `.opus` y `.ogg` de WhatsApp a MP3 directamente en el navegador.

- Usa **Web Audio API** nativa del browser para decodificar el audio
- Usa **lamejs** (encoder MP3 en JavaScript puro) para la conversión
- El archivo nunca sale del dispositivo del usuario
- Sin SharedArrayBuffer, sin Workers externos, sin headers COOP/COEP
- Compatible con Chrome, Edge, Firefox y Safari

### 2. Generador de Link WhatsApp + QR
**URL:** `/link-whatsapp.html`

Genera links `wa.me` personalizados con mensaje predefinido, código QR descargable y botón HTML.

- Generación en tiempo real mientras el usuario escribe
- QR descargable como PNG con fondo blanco (260×260px)
- Snippet HTML del botón listo para pegar en cualquier web
- 25 países de LATAM y España preconfigurados
- 6 plantillas de mensaje rápidas
- Usa **qrcodejs** desde CDN de Cloudflare

---

## Artículos de Blog (SEO)

| Archivo | Keyword objetivo |
|---------|-----------------|
| `/blog/como-crear-link-whatsapp-sin-guardar-numero.html` | link whatsapp sin guardar numero |
| `/blog/convertir-audio-whatsapp-mp3.html` | convertir audio whatsapp mp3 |
| `/blog/que-es-formato-opus-whatsapp.html` | que es formato opus whatsapp |

---

## Stack Técnico

| Capa | Tecnología |
|------|-----------|
| Frontend | HTML5, CSS3, JavaScript vanilla |
| Audio | Web Audio API + lamejs@1.2.1 |
| QR | qrcodejs@1.0.0 (Cloudflare CDN) |
| Fuentes | Google Fonts (Syne + DM Sans) |
| Servidor | Nginx en Ubuntu 24.04 |
| Hosting | Contabo VPS (109.199.114.100) |
| Dominio | GoDaddy → watools.online |
| SSL | Let's Encrypt (Certbot, auto-renovable) |

---

## Estructura del Proyecto

```
watools/
├── index.html                          # Herramienta 1: Audio → MP3
├── link-whatsapp.html                  # Herramienta 2: Generador Link + QR
├── favicon.svg                         # Favicon SVG inline
├── robots.txt                          # Reglas para crawlers
├── sitemap.xml                         # Sitemap con 5 URLs + imágenes
├── site.webmanifest                    # PWA manifest
└── blog/
    ├── como-crear-link-whatsapp-sin-guardar-numero.html
    ├── convertir-audio-whatsapp-mp3.html
    └── que-es-formato-opus-whatsapp.html
```

---

## SEO Técnico Implementado

- Schema JSON-LD completo en `@graph`: `Organization`, `WebSite`, `WebPage`, `BreadcrumbList`, `WebApplication`, `HowTo`, `FAQPage`
- Meta tags: `title`, `description`, `keywords`, `canonical`, `hreflang es/es-419/x-default`
- Open Graph completo + Twitter Card `summary_large_image`
- `sitemap.xml` con `image:image`, `xhtml:link` hreflang, `lastmod`, `priority`
- Estructura H1/H2/H3 correcta con keywords principales
- Atributos `aria-label`, `aria-hidden`, `role` en elementos interactivos
- Internal links entre todas las páginas
- Texto SEO de 300+ palabras por página con keywords naturales
- `robots.txt` bloqueando solo URLs sin valor SEO

---

## Configuración del Servidor

### Nginx (`/etc/nginx/sites-available/watools`)

```nginx
server {
    listen 80;
    server_name watools.online www.watools.online;
    root /var/www/watools;
    index index.html;

    gzip on;
    gzip_types text/html text/css application/javascript application/json image/svg+xml;

    location ~* \.(js|css|png|svg|ico|woff2|xml|webmanifest)$ {
        expires 1y;
        add_header Cache-Control "public, immutable";
    }

    location ~* \.html$ {
        add_header Cache-Control "no-cache, must-revalidate";
    }

    location / {
        try_files $uri $uri/ =404;
    }
}
```

### HTTPS

```bash
certbot --nginx -d watools.online -d www.watools.online
```

Certificado Let's Encrypt con renovación automática cada 90 días.

---

## Deploy

Subir archivos al servidor via WinSCP o SCP:

```bash
scp -r * root@109.199.114.100:/var/www/watools/
```

Recargar Nginx después de cambios en configuración:

```bash
systemctl reload nginx
```

---

## Monetización

- **Google AdSense** — aplicar cuando el sitio tenga 4-6 semanas de tráfico orgánico
- **RPM estimado:** $3-8 USD por cada 1,000 visitas (tráfico LATAM en español)
- **Proyección año 1:** $120-$400/mes al alcanzar 30k-80k visitas mensuales

---

## Google Search Console

- **Propiedad verificada:** `https://watools.online/`
- **Método de verificación:** Archivo HTML
- **Sitemap enviado:** `/sitemap.xml` — 5 páginas descubiertas
- **Estado actual:** Indexación en proceso (sitio lanzado marzo 2026)

---

### Por qué es 100% estático
Sin backend = sin costos de servidor adicionales, sin mantenimiento de APIs, sin base de datos. Todo el procesamiento ocurre en el browser del usuario. Costo operativo: ~$6/mes (VPS Contabo).

---

## Autor

**Julio Cesar Marte Sosa**  
Desarrollador .NET Full Stack  
Santo Domingo, República Dominicana  
[GitHub](https://github.com/esosa772) · [LinkedIn](#)
