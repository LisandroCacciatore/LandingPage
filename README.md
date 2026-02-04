# Lisandro Cacciatore - Website

Sitio web personal enfocado en ingeniería de datos para deporte de alto rendimiento.

## 📁 Estructura de Archivos

```
.
├── index.html              # Página principal
├── blog.html               # Índice de artículos
├── style_v3.css           # Estilos globales
├── .gitignore
│
├── blog/                   # Artículos del blog
│   ├── dashboards-que-no-responden.html
│   ├── datos-deportivos.html
│   ├── gps-data-quality.html
│   ├── seo-aeo-geo.html
│   └── templateBlog.html
│
├── tools/                  # Páginas de detalle de productos
│   └── session-qa-checklist.html
│
└── img/                    # Assets visuales
    └── (tus imágenes)
```

## 🚀 Deployment

### Opción 1: GitHub Pages (Gratis)
1. Subir todo el contenido a un repo de GitHub
2. Ir a Settings > Pages
3. Seleccionar branch `main` y carpeta `/ (root)`
4. Tu site estará en `https://tu-usuario.github.io/nombre-repo`

### Opción 2: Netlify (Gratis, con dominio custom)
1. Conectar repo de GitHub a Netlify
2. Deploy automático en cada push
3. Configurar dominio custom en DNS settings

### Opción 3: Servidor tradicional (cPanel/FTP)
1. Subir todos los archivos vía FTP
2. Asegurarse de mantener la estructura de carpetas
3. Configurar dominio en el hosting

## 📝 Notas Importantes

### Enlaces internos
Todos los enlaces usan rutas relativas:
- Desde raíz a blog: `blog/nombre-archivo.html`
- Desde blog a raíz: `../index.html`
- Desde blog a tools: `../tools/nombre-archivo.html`

### Imágenes
Las rutas de imágenes en `index.html` apuntan a:
```html
<img src="img/Foto0A.jpg" alt="...">
```

Asegurate de que la carpeta `img/` contenga:
- Foto0A.jpg (hero image)
- Banner01.png, Banner02.png
- Foto19.jpg, Foto20.png, Foto21.jpg

### Secciones del Index

1. **Hero** - Propuesta de valor principal
2. **Problemas** - Pain points del público objetivo
3. **Soluciones** (#soluciones) - Qué construís
4. **Servicios** (#servicios) - Ofertas de consultoría
5. **Tools** (#tools) - Productos digitales (USD 3-7)
6. **Academia** (#recursos) - Formación
7. **Contacto** (#contacto) - CTA principal

## 🔗 URLs importantes a configurar

Cuando tengas el dominio definitivo, actualizar:
- Link de "Academia" → `https://academy.lisandrocacciatore.com`
- Email en footer → tu email real
- Links de "Comprar" en tools → pasarela de pago

## 🛠️ Mantenimiento

### Para agregar un nuevo post:
1. Copiar `blog/templateBlog.html`
2. Renombrar con formato: `nombre-del-post.html` (con guiones)
3. Completar metadata, título, contenido
4. Agregar card en `blog.html` con la categoría correcta

### Para agregar una nueva tool:
1. Crear página en `tools/nombre-tool.html`
2. Seguir estructura de `session-qa-checklist.html`
3. Agregar card en sección `#tools` de `index.html`

## ✅ Checklist Pre-Launch

- [ ] Verificar que todas las imágenes carguen correctamente
- [ ] Probar todos los enlaces internos
- [ ] Configurar Google Analytics (agregar tracking code)
- [ ] Probar responsive en mobile
- [ ] Configurar meta tags de Open Graph para shares
- [ ] Revisar ortografía en español
- [ ] Configurar favicon
- [ ] Agregar sitemap.xml
- [ ] Configurar robots.txt

## 📊 Métricas clave a trackear

1. Páginas más visitadas
2. Conversión de blog → tools
3. Conversión de tools → contacto
4. Tasa de rebote en cada sección
5. Tiempo en página (especialmente posts)

## 🔒 Seguridad

- Todos los links externos usan `target="_blank"` solo cuando es necesario
- No hay código JavaScript de terceros no confiables
- CSS inline solo donde mejora performance
- No se almacenan datos sensibles en el frontend

---

**Última actualización:** Febrero 4, 2026  
**Versión:** 1.0  
**Contacto:** [Tu email o forma de contacto]
