# Proyecto final modulo 3

Este es el proyecto final del módulo 3 del bootcamp. El proyecto consiste en una página web para la empresa Bizmate, que incluye las siguientes secciones: Header, Main, Products y Footer.

## Estructura del Proyecto

### Header

El header contiene la barra de navegación fija en la parte superior de la página. Incluye el logo de la empresa y el menú principal del sitio web: “Inicio”, “Nosotros”, “Productos” y “Contacto”. La barra de navegación cambia de apariencia cuando se realiza scroll en la página, mostrando el logo transparente.

### Main

La sección principal (Main) incluye información sobre la empresa Bizmate. Se presenta una imagen en la sección izquierda y una descripción de la empresa a la derecha, destacando su experiencia y servicios. También se incluye una lista con los puntos clave de los servicios ofrecidos y un formulario para que los usuarios ingresen su correo electrónico y se pongan en contacto con la empresa.

### Products

La sección de productos muestra los diferentes productos que ofrece Bizmate. Cada producto se presenta en una tarjeta (card) de Bootstrap, que incluye una imagen, un título, una breve descripción y un botón para ver más detalles. 

### Footer

El footer contiene información de contacto de la empresa, una lista de las secciones del sitio web y una breve descripción sobre la empresa. También incluye iconos de redes sociales que enlazan a las páginas de Twitter, Facebook, YouTube y LinkedIn.

## Tecnologías Utilizadas

- **HTML5**: Para la estructura del contenido de la página web.
- **CSS3**: Para los estilos y la apariencia visual de la página web.
- **Bootstrap 4.5**: Específicamente para las tarjetas (cards) de los productos en la sección Products.
- **JavaScript**: Para cambiar la apariencia de la barra de navegación (navbar) cuando se hace scroll en la página web.

## Descripción del Script de JavaScript

El script de JavaScript se utiliza para cambiar la apariencia de la barra de navegación (navbar) cuando se hace scroll en la página web. Específicamente, agrega y elimina una clase CSS llamada `scrolled` al navbar dependiendo de la posición de desplazamiento del scroll en la página web. Además, oculta y muestra el logo de la empresa en la barra de navegación.

```javascript
$(window).scroll(function() {
    if ($(this).scrollTop() > 50) {
        $('.navbar').addClass('scrolled');
        $('#logo').hide();
        $('#logo-transparente').show();
    } else {
        $('.navbar').removeClass('scrolled');
        $('#logo').show();
        $('#logo-transparente').hide();
    }
});
