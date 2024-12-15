# P.FINAL Portfolio

> S2DAW Diseño Web
> Autor: Lucas Hernández

## 1. Descripción

Esta es mi portfolio, he decidido hacerlo simple con colores "empresariales". Hecho usando **Vite** para la programación, **SCSS** para los estilos y **GitHub** para el control de versiones y **Pages** para el despliegue de la propia web.
La estructura del proyecto es la siguiente:

![ruta](assets/Captura%20de%20pantalla%202024-12-14%20141117.png "")




Al hacer click en los botones de la NavBar te redirecciona cada parte de la página usando enlaces al id de la sección
```markdown
<a href="#about">About</a>
```
Y el Título de Porfolio te lleva arriba de la página

El NavBar se queda fija arriba de la página usando posicion fijada


```markdown
#nav-bar {
  height: auto;
  width: 100%;
  position: fixed;
  z-index: 100;
  background-color: $color-negro;
}
```
Al pulsar el botón de Download CV se descarga mi Cv


```markdown
      <a type="button" class="about-info-button" href="assets/Lucas_Hernandez_CV.pdf" download="Lucas_Hernandez_CV">
        Download CV
      </a>
```

En la parte de Career he hecho unas tarjetas con animación que describen algunos proyectos que he hecho y mi experiencia laboral

```markdown
<div class="service">
        <div class="service-card">
          <div class="service-front">
            <i class="fa fa-laptop-code"></i>

            <h1 class="service-front-heading">Back-end Dev</h1>
          </div>
          <div class="service-back">
            <h1 class="service-back-heading">Library app</h1>
            <p class="service-back-desc">I have developed a fully functional Library application with user management
              and database access, a shopping cart application with order placement, and several applications with
              filters and sorting features. </p>


          </div>
        </div>
      </div>
```
Con el siguiente diseño:

```markdown
 .service-card {
        position: absolute;
        height: 100%;
        width: 100%;
        transform-style: preserve-3d;
        transition: 0.3s ease transform;
        display: block;

        .service-front,
        .service-back {
          position: absolute;
          left: 0;
          top: 0;
          height: 100%;
          width: 100%;
          backface-visibility: hidden;
          display: flex;
          flex-direction: column;
          align-items: center;
          justify-content: center;
          background-color: rgba(0, 0, 0, 0.13);
          padding: 10px;
        }
        }
```

Con el boton Contact Me, te lleva tu aplicación de correo electrónico para que me puedas 

```markdown
<a href="mailto:alumno.648806@ies-azarquiel.es?subject=Buenos%20dias%20Lucas&body=Este%20es%20un%20mensaje%20de%20prueba"
      class="hire-button">
      Contact Me !!
    </a>
```
En el footer los iconos de LinkedIn, GitHub y X te llevan a mis respectivos perfiles. 

![ruta](assets/Captura%20de%20pantalla%202024-12-14%20132403.png "")


## 3. Secciones del diseño


En ["_header.scss"](styles/_header.scss) estilé el NavBar con animaciones cuando pasas el ratón por encima. el NavBar se comprime en un "hamburguer menu" para cuando se visite desde dispositivos móviles:

![ruta](assets/Captura%20de%20pantalla%202024-12-14%20143147.png "")


 En ["_layout.scss"](styles/_layout.scss) está la parte main de la página.

En ["_footer.scss"](styles/_footer.scss) están los iconos de las redes sociales usando iconos Font Awesome

```markdown
        <a href="https://www.linkedin.com/in/lucas-hernandez-140a03292/"><i class="fab fa-linkedin"></i></a>
        <a href="#"><i class="fab fa-twitter"></i></a>
        <a href="https://github.com/luchernan"><i class="fab fa-github"></i></a>

 ```

 En ["_variables.scss"](styles/_variables.scss) están todas las variables que he usado, tanto como colores, fuentes y tamaños.

En ["_mixins.scss"](styles/_mixins.scss) están los tamaños para implementar las mediaquerys (he tenido problemas con los breakpoints y los he dejado comentados en el layout.scss) para el diseño movil, que he cambiado en cada etiqueta y clase lo imprescindible para que se vea bien tanto en mi portatil como en el iPhone 14 pro usando el plugin de Chrome Responsive Viewer.




## 4. Implementacion librería Js

He implementado la librería AOS para las animaciones de la web


## 5. Enlaces de interés

[Enlace a la página desplegada en GitHub Pages](https://luchernan.github.io/vite-project1/)

[Enlace al diseño en Figma](https://www.figma.com/design/cDocnmiPRzu4RgK7e3Fwhj/Untitled?node-id=0-1&t=OOTPHuWWmNrJbEB4-1)
