## Descripción

Este proyecto es un preloader simple y elegante implementado completamente con HTML y CSS. Los preloaders son una excelente manera de mejorar la experiencia del usuario al proporcionar una indicación visual de que el contenido se está cargando.

## Características

- 100% HTML y CSS, sin JavaScript.
- Compatible con todos los navegadores modernos.
- Diseño responsivo.
- Fácil de integrar en cualquier proyecto web.

## Vista Previa

Puedes ver una demostración en vivo [aquí](https://codepen.io/JoaqinSotelo/pen/MWddEGK).

## Uso

### Instrucciones de Integración

1. **HTML:** Añade el siguiente código en el cuerpo (`<body>`) de tu documento HTML.

    ```html
    <div class="preloader-wrapper">
      <div class="preloader"></div>
    </div>
    ```

2. **CSS:** Añade el siguiente código en tu archivo CSS o en una etiqueta `<style>` dentro del `<head>` de tu HTML.

    ```css
    /* Preloader CSS */
    body {
    background-color: rgb(6, 7, 7);
    }
    .preloader-wrapper {
    width: 100%;
    height: 100vh;
    margin: 0 auto;
    position: absolute;
    top: 0;
    left: 0;
    z-index: 111;
    background: #fff;
    }
    .preloader-wrapper .preloader {
    margin: 20% auto 0;
    transform: translateZ(0);
    }
    .preloader:before,
    .preloader:after {
    content: '';
    position: absolute;
    top: 0;
    }
    .preloader:before,
    .preloader:after,
    .preloader {
    border-radius: 50%;
    width: 2em;
    height: 2em;
    animation: animation 1.2s infinite ease-in-out;
    }
    .preloader {
    animation-delay: -0.16s;
    } 
    .preloader:before {
    left: -3.5em;
    animation-delay: -0.32s;
    }
    .preloader:after {
    left: 3.5em;
    }
    @keyframes animation {
    0%,
    80%,
    100% {
      box-shadow: 0 2em 0 -1em red;
    }
    
    40% {
      box-shadow: 0 2em 0 0 red;
    }
    }
    ```

3. **JavaScript (Opcional):** Puedes añadir el siguiente código JavaScript para ocultar el preloader una vez que la página haya terminado de cargar.

    ```html
    <script>
    window.addEventListener('load', function () {
        document.querySelector('.preloader').style.display = 'none';
    });
    </script>
    ```
