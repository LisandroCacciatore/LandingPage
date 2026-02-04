# 📂 Estructura Visual del Website

```
lisandro-cacciatore-website/
│
├── 📄 index.html                    ← Página principal con sección Servicios
├── 📄 blog.html                     ← Índice de todos los posts
├── 🎨 style_v3.css                  ← Estilos globales (no modificar)
├── 📝 .gitignore                    ← Git ignore rules
├── 📘 README.md                     ← Instrucciones generales
├── 📋 VERSION_NOTES.md              ← Changelog completo
├── ✅ DEPLOYMENT_CHECKLIST.md       ← Paso a paso para deploy
├── 📊 CAMBIOS_IMPLEMENTADOS.md      ← Resumen de cambios
│
├── 📁 blog/                         ← Todos los artículos
│   ├── 📄 dashboards-que-no-responden.html    ✨ NUEVO
│   ├── 📄 gps-data-quality.html               ✨ NUEVO
│   ├── 📄 datos-deportivos.html               (Guía Maestra)
│   ├── 📄 seo-aeo-geo.html                    (SEO/AEO/GEO)
│   └── 📄 templateBlog.html                   (Template para futuros posts)
│
├── 📁 tools/                        ← Páginas de productos digitales
│   └── 📄 session-qa-checklist.html           ✨ NUEVO (USD 3)
│
└── 📁 img/                          ← Assets visuales
    ├── 📝 README_IMAGENES.md        ← Instrucciones de qué imágenes subir
    │
    └── (Tus imágenes van aquí:)
        ├── 🖼️ Foto0A.jpg            ← Hero image principal
        ├── 🖼️ Banner01.png          ← Caso de estudio 1
        ├── 🖼️ Banner02.png          ← Caso de estudio 2
        ├── 🖼️ Foto19.jpg            ← Sección proceso
        ├── 🖼️ Foto20.png            ← Sección diferencial
        └── 🖼️ Foto21.jpg            ← Testimonial/caso
```

---

## 🔗 Mapa de Enlaces

### Desde `index.html` (raíz)
```
index.html
├─→ blog.html
├─→ blog/dashboards-que-no-responden.html
├─→ blog/gps-data-quality.html
├─→ blog/datos-deportivos.html
├─→ tools/session-qa-checklist.html
└─→ img/Foto0A.jpg
```

### Desde `blog/` (artículos)
```
blog/dashboards-que-no-responden.html
├─→ ../index.html                      (botón "Inicio")
├─→ ../blog.html                       (botón "Volver al Hub")
├─→ ../tools/session-qa-checklist.html (CTA del post)
└─→ ../img/...                         (si usa imágenes)
```

### Desde `tools/` (productos)
```
tools/session-qa-checklist.html
├─→ ../index.html                      (navegación principal)
├─→ ../blog.html                       (si linkea a posts)
└─→ ../index.html#contacto             (CTA consultoría)
```

---

## 📍 Secciones del Index (Anclas)

Estos son los IDs de sección para navegación interna:

```html
index.html
├─→ #hero              (Landing principal)
├─→ #problemas         (Pain points)
├─→ #soluciones        (Qué construís)
├─→ #diferencial       (Por qué yo)
├─→ #casos             (Casos reales)
├─→ #pricing           (Planes y precios)
├─→ #servicios         ✨ NUEVO (Consultoría)
├─→ #tools             (Marketplace de productos)
├─→ #recursos          (Academia)
└─→ #contacto          (Footer CTA)
```

---

## 🎯 Embudo de Conversión

### Flujo 1: Validación de Datos
```
Usuario entra por Google
        ↓
"Por qué tus datos GPS son basura" (blog/gps-data-quality.html)
        ↓
CTA: "Session QA Checklist" (tools/session-qa-checklist.html)
        ↓
Cross-sell: "Setup de sistema de datos" (index.html#servicios)
        ↓
Conversión: (index.html#contacto)
```

### Flujo 2: Dashboards
```
Usuario entra desde LinkedIn
        ↓
Landing (index.html) - Sección "Dashboards que no responden"
        ↓
Click: "Leer artículo" → (blog/dashboards-que-no-responden.html)
        ↓
CTA: "Training Load Dashboard" (index.html#tools)
        ↓
Cross-sell: "Análisis de rendimiento mensual" (index.html#servicios)
        ↓
Conversión: (index.html#contacto)
```

---

## 🚀 Orden de Deploy

### Paso 1: Preparar archivos locales
1. Descargar todos los archivos de `/outputs`
2. Agregar tus imágenes a carpeta `/img`
3. Revisar que todos los enlaces funcionen localmente

### Paso 2: Subir a servidor
```bash
# Opción A: Git + GitHub Pages
git init
git add .
git commit -m "Initial website deployment"
git push origin main

# Opción B: FTP (mantener estructura exacta)
/public_html/
├── index.html
├── blog.html
├── style_v3.css
├── blog/
├── tools/
└── img/
```

### Paso 3: Verificar
1. Abrir `tudominio.com` o `usuario.github.io`
2. Navegar a cada sección
3. Probar todos los links
4. Verificar que imágenes cargan
5. Testear en mobile

---

## 📊 Archivos por Tipo

### HTML (10 archivos)
- ✅ index.html
- ✅ blog.html
- ✅ blog/dashboards-que-no-responden.html
- ✅ blog/gps-data-quality.html
- ✅ blog/datos-deportivos.html
- ✅ blog/seo-aeo-geo.html
- ✅ blog/templateBlog.html
- ✅ tools/session-qa-checklist.html

### CSS (1 archivo)
- ✅ style_v3.css

### Markdown (5 archivos - documentación)
- ✅ README.md
- ✅ VERSION_NOTES.md
- ✅ DEPLOYMENT_CHECKLIST.md
- ✅ CAMBIOS_IMPLEMENTADOS.md
- ✅ img/README_IMAGENES.md

### Config (1 archivo)
- ✅ .gitignore

### Imágenes (pendientes)
- ⏳ img/Foto0A.jpg
- ⏳ img/Banner01.png
- ⏳ img/Banner02.png
- ⏳ img/Foto19.jpg
- ⏳ img/Foto20.png
- ⏳ img/Foto21.jpg

---

## ✨ Qué Hace Cada Archivo Principal

### `index.html`
- Hero con propuesta de valor
- Sección de problemas
- Soluciones técnicas
- **✨ NUEVA: Sección Servicios** (consultoría)
- Marketplace de tools (USD 3-7)
- Academia y recursos
- Contacto

### `blog.html`
- Índice filtrable de posts
- Categorías: Datos, Automatización, Arquitectura, Dashboards
- **✨ NUEVO: Post destacado** "Dashboards que no responden"

### `blog/dashboards-que-no-responden.html`
- Post completo sobre dashboards
- Problema → Solución → CTA a tool
- SEO optimizado
- Cross-link a productos

### `blog/gps-data-quality.html`
- Post sobre validación de datos GPS
- Scripts Python incluidos
- CTA a Session QA Checklist
- Cross-link a guía maestra

### `tools/session-qa-checklist.html`
- Página de producto completa
- Descripción del problema
- Qué incluye (USD 3)
- FAQs
- Cross-sell a consultoría

---

## 🎨 Paleta de Colores (de style_v3.css)

```css
--primary-blue: #0066CC      /* Enlaces y CTAs principales */
--text-dark: #1e293b         /* Texto principal */
--text-body: #475569         /* Texto secundario */
--text-muted: #64748b        /* Texto terciario */
--bg-soft: #f8fafc           /* Fondos suaves */
--border-color: #e2e8f0      /* Bordes y separadores */
```

No modificar estos valores sin actualizar todo el diseño.

---

## 📱 Responsive

Todos los archivos están optimizados para:
- ✅ Desktop (1920px+)
- ✅ Laptop (1366px)
- ✅ Tablet (768px)
- ✅ Mobile (375px)

Testing realizado en Chrome DevTools.

---

**Última actualización:** Febrero 4, 2026  
**Total de archivos:** 17 (sin contar imágenes)  
**Estado:** ✅ Listo para deploy
