# CONTRIBUTING

La carpeta `version-con-bulma/` debe replicar la estructura visual y la lógica de contenido de la versión en Tailwind, usando clases de Bulma en lugar de utilidades de Tailwind.

Se trabaja principalmente sobre estos archivos:

- `version-con-bulma/index.html`
- `version-con-bulma/detalle_producto.html`



## 3. Reglas para contribuir
- mismo formato de comentarios que version-con-tailwind
- no modificar version-con-tailwind

### 3.1. Mantener la estructura visual

La versión de Bulma debe respetar:

- misma paleta de colores
- misma jerarquía visual
- mismo contenido textual
- misma disposición en columnas y bloques
- misma semántica de secciones


### 3.2 Importante

La versión no necesita ser idéntica pixel a pixel, pero sí debe mantener la misma intención de diseño y el mismo orden de contenido.

### 3.3. No romper rutas de archivos

Todos los recursos deben apuntar correctamente a la estructura local:

- `Img/...`
- `css/estilos.css`

Ejemplo correcto:

```html
<link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/bulma@1.0.4/css/bulma.min.css">
<link rel="stylesheet" href="css/estilos.css">
<img src="Img/img-logos/img-logo-pagina/logo.png" alt="God Gaming">
```

## 4. Qué debe completar `index.html`

La página principal debe incluir estas secciones, en este orden:

### 4.1. Header

Requerido:

- logo de la marca
- iconos de carrito y perfil
- buscador de productos
- barra de categorías:
  - Mousepad
  - Teclado
  - Mouse
  - Auriculares

Debe quedar responsive, con el buscador y los iconos alineados correctamente en mobile y desktop.

### 4.2. Banner principal

Debe incluir una imagen promocional del banner:

- `Img/img-banner/banner-1.png`

Se puede envolver en un `section` con imagen de fondo o una imagen completa.

### 4.3. Productos en oferta

Esta sección debe mostrar 4 cards:

1. Auriculares Logitech G PRO X2 Wireless
2. Mouse Razer DeathAdder V4 PRO Wireless
3. Mouse Pad SteelSeries QCK XXL
4. Teclado HyperX Alloy Rise RGB

Cada tarjeta debe tener:

- imagen del producto
- nombre
- precio tachado
- precio actual
- botón Comprar

### 4.4. Banner de envío gratis

Debe incluir la imagen:

- `Img/img-banner/banner-2.png`

### 4.5. Sección de productos

Debe mostrar una grilla con productos adicionales.

Recomendado: 8 productos con la misma lógica visual que la referencia.

### 4.6. Reseñas de usuarios

Debe incluir 4 reseñas con:

- foto de avatar
- nombre del cliente
- producto comprado
- breve comentario

Imágenes esperadas:

- `Img/img-reseña/reseña1.png`
- `Img/img-reseña/reseña2.png`
- `Img/img-reseña/reseña3.png`
- `Img/img-reseña/reseña4.png`

### 4.7. Preguntas frecuentes

Debe incluir al menos dos columnas con preguntas sobre:

- Envíos
- Devoluciones

Cada item puede ser una fila con texto y un botón/ícono de suma.

### 4.8. Footer

Debe contener:

- Información
  - Políticas de Devolución
  - Política de Privacidad
  - Términos y Condiciones
- Ubicación
- Contacto
  - teléfono
  - email
  - redes sociales
- Pie de copyright

## 5. Qué debe completar `detalle_producto.html`

La página del producto debe seguir la estructura de la referencia de Tailwind y completar la información del producto principal.

### 5.1. Header para detalle del producto

Debe mantener la misma barra superior:

- logo
- carrito
- perfil
- buscador
- categorías

### 5.2. Galería de imágenes del producto

Debe existir una columna izquierda con:

- imagen principal del producto
- miniaturas debajo

Producto principal:

- `Img/img-productos/img-auriculares/Imganen_Auriculares_Logitech_PRO_X_2_Wireless.jpg`

Miniaturas:

- `Img/img-productos/img-auriculares/detalle_producto/detalle_producto/compragamer_Imganen_general_39727_Auriculares_Logitech_PRO_X_2_2.jpg`
- `Img/img-productos/img-auriculares/detalle_producto/detalle_producto/compragamer_Imganen_general_39728_Auriculares_Logitech_PRO_X_2_3.jpg`
- `Img/img-productos/img-auriculares/detalle_producto/detalle_producto/compragamer_Imganen_general_39729_Auriculares_Logitech_PRO_X_2_4.jpg`

### 5.3. Información del producto

Debe incluir:

- título del producto
- SKU y ID
- precio original tachado
- precio final
- estado de stock
- botón "Comprar ahora"
- bloque de medios de pago
- bloque de garantías y envíos
- enlace a términos y condiciones

Texto base esperado:

```text
Auriculares Logitech G PRO X2 Wireless Lightspeed
2.4Ghz Bluetooth Black Audio 7.1 50Hs PC/PS4/PS5
```

### 5.4. Especificaciones técnicas

Debe mostrar una sección con características generales, por ejemplo:

- Compatibilidad: PC, PS4, PS5
- Audio: Sonido envolvente 7.1
- Duración de la batería: Hasta 50 horas
- Micrófono: Micrófono con cancelación de ruido extraíble
- Control de audio: Controles en el auricular para volumen y micrófono
- Diseño: Diadema ajustable y almohadillas viscoelásticas
- Colores disponibles: Negro / Blanco

### 5.5. Footer del producto

Debe mantener el mismo estilo del footer del ecommerce:

- Información
- Ubicación
- Contacto
- teléfono
- email
- redes sociales

## 6. Estilo recomendado para Bulma

Para completar la interfaz sin perder consistencia, se recomienda trabajar con estas convenciones:

- `section` para áreas grandes
- `container` para limitar contenido
- `columns` y `column` para grillas
- `box` para tarjetas y panels
- `button is-primary` o `button is-link` para CTA
- `media` para reseñas y contenido editorial
- `footer` para pie de página
- `image is-128x128` o `figure` para imágenes


## 7. Checklist de aceptación

### Para `index.html`

- [ ] Header completo con logo, buscador y categorías
- [ ] Banner principal visible
- [ ] Sección de ofertas con 4 cards
- [ ] Banner de envío gratis
- [ ] Grilla de productos
- [ ] Reseñas con 4 tarjetas
- [ ] FAQ con dos categorías
- [ ] Footer con información y contacto
- [ ] Diseño responsive

### Para `detalle_producto.html`

- [ ] Header consistente con la home
- [ ] Galería de imágenes con miniaturas
- [ ] Información del producto con precio y stock
- [ ] Botón de compra principal
- [ ] Bloques de pago, envío y garantía
- [ ] Sección de especificaciones técnicas
- [ ] Footer final
- [ ] Layout legible y ordenado en desktop y mobile

## 8. Buenas prácticas

- mantener nombre de clases claros y reutilizables
- evitar CSS 
- no inventar contenido sin sentido; mantener el texto del ecommerce
- usar `alt` en todas las imágenes
- revisar rutas relativas antes de cerrar la tarea
- mantener consistencia entre `index.html` y `detalle_producto.html`

## 9. Flujo sugerido de trabajo

1. abrir `version-con-bulma/index.html`
2. completar estructura principal del header
3. completar ofertas y productos
4. validar secciones de reviews y FAQ
5. cerrar footer
6. abrir `version-con-bulma/detalle_producto.html`
7. completar galería y panel de compra
8. cerrar especificaciones y footer
9. probar en navegador
10. revisar que no haya rutas rotas ni errores visuales

## 10. Criterio final

La tarea está terminada cuando la versión Bulma:

- refleja la misma estructura que la de tailwind
- mantiene los mismos bloques de contenido del proyecto
- funciona visualmente en mobile y desktop
- usa Bulma de manera natural y limpia
- no presenta rutas ni elementos rotos


