# tienda-online-web



README.md (lista para pegar)
Huachumascota — Tienda demo (Apizaco, Tlaxcala)
Breve: Sitio estático de catálogo de ropa y/o accesorios pensado para desplegar en GitHub Pages o cualquier hosting estático. Proyecto educativo y de portafolio, listo para personalizar imágenes, precios y descripciones.

Estructura del repo
index.html — frontend estático

/data/products.json — listado de productos consumido por la interfaz

/images/ — imágenes de producto (nombres limpios, minúsculas)

/assets/ — logo y otros assets

README.md — este archivo

LICENSE — licencia del proyecto

Cómo funciona
El frontend carga /data/products.json al iniciar y renderiza cards de producto en la página.

Imágenes locales deben estar en /images/ y la ruta en el JSON debe apuntar a images/nombre.jpg.

No requiere backend para mostrarse; para guardar/editar productos en producción necesitas un servicio (Azure Blob, API, o commits al repo vía GitHub API).

products.json (ejemplo mínimo)
json
[
  {
    "id": 1,
    "title": "Vestido Floral",
    "price": 299.00,
    "currency": "MXN",
    "image": "images/vestido-floral.jpg",
    "category": "Vestidos",
    "description": "Vestido ligero de algodón, ideal para verano.",
    "stock": 12,
    "sku": "HU-VF-001",
    "slug": "vestido-floral"
  }
]
Añadir o actualizar productos
Agrega la imagen a /images/ (800×800 para card, 400×400 para thumbs opcional).

Edita /data/products.json y añade/actualiza objetos JSON.

Haz commit y push al repo; GitHub Pages servirá la versión actual.

Despliegue en GitHub Pages (rápido)
Crea repo en la organización.

Sube archivos (index.html, data/, images/, assets/).

En Settings → Pages activa la rama main (root).

Accede a https://<org>.github.io/<repo>/.

Opciones de alojamiento de imágenes y JSON
GitHub raw: https://raw.githubusercontent.com/tu-org/tu-repo/main/images/archivo.jpg (útil para pruebas).

Azure Blob Storage: recomendado para producción y escalabilidad.

CDN: mejora rendimiento en producción.

Prototipado de pedidos sin backend
Botón "Pedir por WhatsApp": abrir enlace https://wa.me/52NUMERO?text=Quiero%20comprar%20{producto}.

Formulario simple: usar Formspree o Netlify Forms para enviar pedidos por correo sin servidor.

Buenas prácticas
No subir credenciales ni archivos sensibles.

Usar .gitignore para builds y secretos.

Optimizar imágenes (WebP/JPG calidad 70–80).

Validar traducciones en lenguas indígenas con hablantes nativos antes de publicar.

Contribuciones
Para cambios envía Pull Request o abre Issues.

Añade un commit claro por cada cambio de producto o mejora en UI.

Licencia y aviso legal
Este proyecto es educativo y de muestra. No contiene sistemas de pago ni manejo de datos sensibles.

Revisa y adapta políticas de privacidad y términos antes de vender en producción.

Traducciones provisionales en náhuatl deben validarse con la comunidad.

Contacto
Proyecto: Huachumascota (o nombre que uses).

Mantén en README los datos de contacto del propietario o un correo de soporte.

LICENSE (MIT) — copia lista para pegar
MIT License

Copyright (c) 2025 TuNombre o NombreDeLaEmpresa

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.
