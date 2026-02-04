# 🚀 Checklist de Deployment - Lisandro Cacciatore Website

## Pre-Deploy

### 1. Archivos y Estructura ✅
- [x] index.html (con sección Servicios)
- [x] blog.html (con nuevo post destacado)
- [x] style_v3.css
- [x] .gitignore configurado
- [x] README.md con instrucciones
- [x] Carpeta `/blog` con 5 posts
- [x] Carpeta `/tools` con Session QA Checklist
- [x] Carpeta `/img` con README de instrucciones

### 2. Imágenes 📸
- [ ] Agregar Foto0A.jpg (hero image)
- [ ] Agregar Banner01.png
- [ ] Agregar Banner02.png
- [ ] Agregar Foto19.jpg, Foto20.png, Foto21.jpg
- [ ] Optimizar todas las imágenes (< 500KB cada una)
- [ ] Verificar que todas cargan correctamente

### 3. Enlaces y Configuración ⚙️
- [ ] Actualizar email en footer de index.html
- [ ] Configurar link de Academia (si existe)
- [ ] Revisar que todos los enlaces internos funcionen
- [ ] Probar navegación en todas las páginas
- [ ] Verificar breadcrumbs en posts de blog

### 4. SEO y Meta Tags 🔍
- [ ] Agregar Google Analytics tracking code
- [ ] Crear y agregar favicon.ico
- [ ] Crear sitemap.xml
- [ ] Crear robots.txt
- [ ] Meta tags Open Graph para shares sociales
- [ ] Verificar meta descriptions en todos los posts

## Deploy Options

### Opción A: GitHub Pages (Recomendada para empezar)

```bash
# 1. Crear repo en GitHub
git init
git add .
git commit -m "Initial commit - Website v1.0"
git branch -M main
git remote add origin https://github.com/tu-usuario/tu-repo.git
git push -u origin main

# 2. Activar GitHub Pages
# Ir a: Settings > Pages
# Seleccionar: branch main, folder / (root)
# Wait 1-2 minutos
# Tu site estará en: https://tu-usuario.github.io/tu-repo
```

**Ventajas:**
- ✅ Gratis
- ✅ HTTPS automático
- ✅ Deploy automático con git push
- ✅ No requiere configuración de servidor

**Desventajas:**
- ⚠️ URL con github.io (a menos que configures dominio custom)
- ⚠️ Solo sitios estáticos (no backend)

---

### Opción B: Netlify (Recomendada para producción)

```bash
# 1. Instalar Netlify CLI
npm install -g netlify-cli

# 2. Login y deploy
netlify login
netlify init
netlify deploy --prod
```

**O bien:**
1. Conectar repo de GitHub en netlify.com
2. Deploy automático en cada push
3. Configurar dominio custom en DNS settings

**Ventajas:**
- ✅ Gratis hasta 100GB bandwidth
- ✅ Dominio custom incluido
- ✅ SSL automático
- ✅ Deploy previews para cada PR
- ✅ Forms nativos sin backend
- ✅ Redirects y headers configurables

---

### Opción C: Vercel (Alternativa a Netlify)

Similar a Netlify, excelente para sitios estáticos.

```bash
npm install -g vercel
vercel login
vercel
```

---

### Opción D: cPanel / FTP (Hosting tradicional)

1. Conectar vía FTP (FileZilla, Cyberduck, etc.)
2. Subir todos los archivos a `/public_html/` o `/www/`
3. Mantener estructura de carpetas exacta
4. Verificar permisos (644 para archivos, 755 para carpetas)

---

## Post-Deploy Checklist

### Inmediatamente después del deploy ⚡
- [ ] Verificar que index.html carga correctamente
- [ ] Probar navegación a todas las secciones
- [ ] Verificar que las imágenes cargan
- [ ] Probar todos los enlaces del menú
- [ ] Revisar en mobile (Chrome DevTools)
- [ ] Verificar en diferentes browsers (Chrome, Firefox, Safari)

### Primera semana 📊
- [ ] Configurar Google Search Console
- [ ] Enviar sitemap.xml a Google
- [ ] Verificar indexación en Google (site:tudominio.com)
- [ ] Revisar Google Analytics (si está configurado)
- [ ] Testear CTAs de contacto
- [ ] Verificar formularios (si los hay)

### Performance y SEO 🚀
- [ ] Run Lighthouse audit (Chrome DevTools)
- [ ] Objetivo: Performance > 90, SEO > 90
- [ ] Verificar tiempos de carga < 3 segundos
- [ ] Revisar Core Web Vitals
- [ ] Testear en conexión lenta (throttling)

---

## Configuración de Dominio Custom

Si tenés dominio propio (ej: `lisandrocacciatore.com`):

### En Netlify:
1. Domain settings > Add custom domain
2. Agregar: `lisandrocacciatore.com` y `www.lisandrocacciatore.com`
3. Netlify te dará DNS records

### En tu proveedor de dominio:
1. Ir a DNS settings
2. Agregar A record:
   ```
   Type: A
   Name: @
   Value: 75.2.60.5 (IP de Netlify, verificar en docs)
   ```
3. Agregar CNAME:
   ```
   Type: CNAME
   Name: www
   Value: tu-sitio.netlify.app
   ```
4. Esperar propagación (1-24 horas)

---

## 🐛 Troubleshooting Común

### "404 Not Found" en rutas internas
**Problema:** Links internos no funcionan después del deploy

**Solución:** Verificar que las rutas sean relativas:
```html
<!-- ✅ Correcto -->
<a href="blog/post.html">Post</a>
<a href="../index.html">Home</a>

<!-- ❌ Incorrecto -->
<a href="/blog/post.html">Post</a>  (asume root del servidor)
```

### Imágenes no cargan
**Problema:** Imágenes rotas (404)

**Solución:** 
1. Verificar que nombres coincidan (case-sensitive)
2. Verificar que carpeta `img/` esté en el root
3. Limpiar caché del browser (Ctrl+Shift+R)

### CSS no aplica
**Problema:** Página sin estilos

**Solución:**
1. Verificar que `style_v3.css` esté en root
2. Verificar link en HTML:
   ```html
   <link rel="stylesheet" href="style_v3.css">
   ```
3. Hard refresh (Ctrl+F5)

---

## 📞 Siguiente Paso: Testeo de Conversión

Una vez deployed, probar el embudo completo:

1. **Landing (index.html):** ¿El mensaje principal es claro?
2. **Problema → Post:** Click en "Dashboards que no responden"
3. **Post → Tool:** Click en CTA "Ver Training Load Dashboard"
4. **Tool → Servicio:** Click en "Consultar" para setup de datos
5. **Servicio → Contacto:** Verificar que el form/email funcione

---

## ✅ Deployment Completado

Cuando todo esté funcionando:

- [ ] Anunciar en LinkedIn
- [ ] Compartir link en redes
- [ ] Enviar a contactos clave
- [ ] Agregar a firma de email
- [ ] Actualizar bio en todas las plataformas

---

**Última actualización:** Febrero 4, 2026  
**Próxima revisión:** 1 mes después del deploy  
**Responsable:** Lisandro Cacciatore
