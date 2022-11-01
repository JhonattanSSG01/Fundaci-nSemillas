# Bienvenidos a la Fundación Semillas 👋👋 !!!
# Sesión Steven

## #Fundación Semillas 🍃🍃
>![image](https://user-images.githubusercontent.com/80645321/199144593-c4a585d1-3309-462f-83cb-7926b24bf274.png)

El dashboard desarrollado para la fundación semillas, se enfoca en solucionar la gran problematica sobre tener un mejor conocimiento frente a las emociones de los estudiantes frente cada actividad realizada en el marco del diplomado.  
#### ***Puedes visualizar la página*** 👉👉 https://neon-sfogliatella-5dfada.netlify.app

## Menú lateral del dashboard 💯
```
<!-- Start Menu lateral -->
<input type="checkbox" id="nav" class="navInput">
<div class="slideBar">
  <!-- Sección logo -->
   <section class="logo">
    'Imagen del logo de la empresa'
   </section>
   <hr>
   <!-- Sección menú de opciones -->
   <nav class="menu">
    <ul>
      <li class="active">
        <a href="">
            'Imagen del estudiante'
            'Nombre del estudinate'
        </a>
      </li>
    </ul>
  </nav>
  <!-- Sección cerrar sesión -->
  <section class="logOut">
    'Botóncerrar sesión
  </section>
</div>
<!-- End menu lateral -->

<!--  Menu hamburguesa -->
<!-- Por el atributo for="nav" llama o cierra al input que tenga el id="nav", en este caso llama al menú lateral -->
<label for="nav" class="icon">
  <section class="icon">
    <hr>
    <hr>
    <hr>
  </section>
</label>
```
```
/* Menú  */
.flexLeft > .slideBar {
  display: block;
  position: absolute;
  top: 4rem;
  bottom: 0;
  left: 0;
  right: 0;
  padding: 0 2%;
  clip-path: polygon(0 0, 0 0, 0 100%, 0 100%);
  transition: 1s;
  background-color: #69bf97;
}

.navInput:checked + .slideBar {
  clip-path: polygon(0 0, 100% 0, 100% 100%, 0 100%);
  transition: 1s;
}
```
En esta parte del código se realizó un menú lateral fijo en la parte izquierda, para poder tener mejor accesibilidad a cada estudiante de la fundación semillas y poder visualizar las gráficas respectivas de cada diplomado en específico. El gran desafío con este menú fue ponerlo al lado izquierdo del contenido principal, al mismo tiempo cuando está en el dispositivo mobile, este se esconde y se despliega solamente cuando se da clic al icono hamburguesa desarrollado con CSS vainilla. La forma que logre solucionar fue poner en un contenedor general todo el contenido principal y darle una posición para lograr moverlo en relación a la ventana del navegador al lado derecho y con tamaño de ancho proporcionado en distintas resoluciones de cada dispositivo para que se acoplen.

Nota: Gracias al input de tipo check box con ID respetivo se logra desarrollar la función de esconder o llamar su hermano más cercano, en este caso es el menú. De igual manera, dentro de label con atributo for se referecnia para realizar la rspectiva conexión al ID del input necesario.

> Desktop y Tablet

![image](https://user-images.githubusercontent.com/80645321/199147577-b4acae72-ebc4-475a-979a-cb051c045d18.png)

> Mobile 

![image](https://user-images.githubusercontent.com/80645321/199147784-ad2e9203-3759-4d81-8255-5de1d748e96e.png)
 
## Pop Up sobre información del estudiante 💯
```
 <!-- Start Pop Up -->
  <div class="containerPopUp">
   <!-- Input con id="student" para llamar a su hermano adyacente, en este caso es el pop up -->
   <input type="checkbox" id="student" class="popIn">
   <!-- Seccion Pop Up -->
   <div class="popUp">
     <!-- Seccion encabezado del pop up -->
      <div class="headerPop">
       
      </div>
      <!-- Seccion cuerpo del pop up -->
       <div class="bodyPop">
         <section class="input">
             'Nombre del estudiante'
             'Biografia del estudiante'
             'Descripcion del estudiante'
         </section>
         <!-- Seccion redes sociales -->
         <section class="socialMedia input">
           'Iconos de las redes sociales'
         </section>
         <!-- Seccion boton -->
         <section class="containerButton">
           <button type="submit">save</button>
         </section>
        </div>
      </div>
    </div>
```
```
/* Pop up */
.popUp {
  width: 95%;
  max-width: 500px;
  height: 50rem;
  border-radius: 0.5rem;
  background-color: rgb(174, 217, 201);
  position: absolute;
  top: 2rem;
  right: 2.8rem;
  transform: rotate(0deg) translate(12%, 12%);
  visibility: hidden;
}

/* Pop up visible */
.popIn:checked + .popUp {
  visibility: visible;
}
```
En esta parte de código se desarrolló el pop up para que solo se visualice cuando sédé clic en la foto del estudiante ya seleccionado en el menú, este aparecerá en cierta posición con lo esperado y cuando se da clic en la x o parte superior del Pop Up este se cerrara. 

Nota: Gracias al input de tipo check box con ID respetivo se logra desarrollar la función de esconder o llamar su hermano más cercano, en este caso es el pop up. De igual manera, dentro de label con atributo for se referecnia para realizar la rspectiva conexión al ID del input necesario.

> ![image](https://user-images.githubusercontent.com/80645321/199152084-26e3e6b7-d8b2-4b00-b233-9c480223a516.png)

## Header estructura 💯
```
<!-- Start Header -->
 <header>
  <div class="containerHeader">
   <!-- Sección menú hamburguesa -->
   <!-- Por el atributo for="nav" llama o cierra al input que tenga el id="nav", en este caso llama al menú lateral -->
    <label for="nav" class="icon">
     <section class="icon">
       'icono del menu hamburguesa'
     </section>
    </label>
    <!-- Sección campo de búsqueda -->
     <section class="search">
      <section class="iconSearch">
        'Icono de lupa'
       </section>
     </section>
     <!-- Sección de usuario -->
     <section class="userFlex">
       <section class="user">
       'Icono del usuario'
       </section>
      /section>
   </div>
 </header>
  <!-- End Header -->
```
En esta parte del código referencia el header del dashboard que abarca un input text para lograr una búsqueda respectiva, su icono se desarrolló con CSS vanilla y lo unico desafuente fueron el tamño de cada item que lo forma, también, está la parte del usuario que al igual que el icono de búsqueda, este se logró realizar con CSs vanilla. Finalmente, en las resoluciones menores a 480px este se fijará en la parte superior para mejor accesibilidad al menú desplegable.

> Desktop y Tablet Grande

![image](https://user-images.githubusercontent.com/80645321/199153670-329139d0-079d-4a75-a2c4-37d24860b8a2.png)

> Mobile Y Tablet pequeña

![image](https://user-images.githubusercontent.com/80645321/199153748-218a890a-2e72-455a-8dca-26e828e1c0de.png)

>Nota: Se le agregó una pequeña animación la cual se escala menos de su tamaño real cuando el cursor pasa encima de él.
```
 .user:hover {
    transform: scale(0.8);
    transition: 2000ms;
  }

  .user:hover .iconUserHead,
  .user:hover .iconUserBody {
    background-color: #009458;
  }
```

## Main Sección tarjetas 🔗🔗
```
 <!-- Start Sección Bienvenida -->
  <div class="welcome">
  <!-- Seccion de foto del estudiante -->
    <section class="photoStudent">
      Imagen del estudiante'
    </section>
    <!-- Seccion de la descripción de Bienvenida -->
    <section class="description">
     'Descripcion sobre las graficas a visaulizar'
    </section>
   </div>
  <!-- End Sección Bienvenida -->
  <!-- Start Sección Diplomados -->
   <div class="agreeContainer">
    <!-- Seccion primera tarjeta -->
      <a href="">
       <div class="agree active">
        'Tarjetas sobre los disferentes diplomados a escoger'
       </div>
      </a> 
   </div>
<!-- End Sección Diplomados -->
```
```
/* Seccion Bienvenida */
.welcome {
  margin: 6.25rem 0 1.9rem 0;
  padding: 0.62rem 0;
  display: flex;
  flex-direction: column;
  align-items: center;
}
```

Esta parte del código abarca una pequeña descripción y tarjetas con la funcionalidad de poder escoger sobre los diplomados respectivos del estudiante, Cada tarjeta tiene información relevante. Su única funcionalidad es ordenarse en filas, es decir, una debajo de otra a la hora de visualizarse en resoluciones menores a 1024px. ya que, mayores a esta resolución se ordenan en columna, es decir, una al lado de otra. 

![image](https://user-images.githubusercontent.com/80645321/199155931-0519e88d-9c85-44b6-901c-20ffa6706a3c.png)

```
<!-- Strat sección gráfica media luna -->
 <div class="stateOfMind">
   <section class="titleState">
     'Titulo principal'
   </section>
   <div class="graphContainer">
    <section class="graphCircle happy">
      'Grafica con su titulo'
    </section>
   </div>
 </div>
```
En esta parte del código se desarrolló las grafica media luna para visualizar el porcentaje general en un diplomado respectivo, esto se logró realizar con la ayuda de los gradientes y rotaciones para obtener lo esperado de una gráfica circular o media luna. Su única funcionalidad es ordenarse en filas, es decir, una debajo de otra a la hora de visualizarse en resoluciones menores a 1024px. ya que, mayores a esta resolución se ordenan en columna, es decir, una al lado de otra. 

## Mian Grafica Lunar o Circular 🔘🔘
```
/* Gráfica media luna */
.graphContainer {
  display: flex;
  flex-direction: column;
  align-items: center;
  flex-wrap: wrap;
}

.graphContainer > .graphCircle {
  position: relative;
  width: 12rem;
  height: 12rem;
  margin: 1rem;
  border-radius: 50%;
  z-index: 1;
}

/* Color Circulo principal */
.graphContainer > .happy {
  background: linear-gradient(125deg, #ff8a00 50%, #000000 50%);
}

.graphContainer > .indifferent {
  background: linear-gradient(90deg, #ff0000 50%, #000000 50%);
}

.graphContainer > .sad {
  background: linear-gradient(45deg, #001aff 50%, #000000 50%);
}

.graphCircle > .circle {
  width: 12rem;
  height: 12rem;
  border-radius: 50%;
  position: absolute;
  top: 0;
  text-align: center;
}

/* Circulo Externo o principal */
.graphCircle > .circleOuter {
  padding: 1em;
  box-sizing: border-box;
  background: #ffffff content-box;
}

/* Circulo interno */
.graphCircle > .circleInner {
  background: linear-gradient(transparent 50%, #ffffff 50%);
  transform: scale(1.1);
}
```
![image](https://user-images.githubusercontent.com/80645321/199156424-f967a083-a37e-426d-aadf-3943e5e6e54a.png)


# Sesion Edward
a mi me toco la parte de hacer una torta con porcentaje y un diagramas de barras  el cual al inicio resulto un poco complicado pero gracias a la ayuda de mis compañeros de logro realizar 
### torta de porcentaje 
esta torta se adapta bien al responsive, tambien tiene una animacion, cada vez que se pasa el cursor por encima de agranda podiendo observarla mejor, algunas partes en el codigo estan comentadas para tener un mejor entendimiento y no perderse en las lineas de codigo
### visual
![imagen](https://user-images.githubusercontent.com/114676009/199132789-ce9a71dd-1b75-4919-84ab-568f632aba77.png)
### codigo html
![imagen](https://user-images.githubusercontent.com/114676009/199132288-906e6d38-d4ff-4d93-a626-64192287e7fb.png)
### codigo css 
![imagen](https://user-images.githubusercontent.com/114676009/199132514-f2499a84-1afc-49e9-895a-58578bdf4f53.png)

### Diagrama de barras 
en este diagramas realizar las barras fue algo sencillo lo mas complicado fue el texto que se encuentra a lado ziquierdo de la grafica puesto que este cuando rotaba era un poco dificil manejarlo, pero al final se pudo lograr y me gusto el resultado final 

### visual
![imagen](https://user-images.githubusercontent.com/114676009/199132756-4f86bc37-ade7-4766-9184-3a311b4c16f7.png)

### codigo Html
![imagen](https://user-images.githubusercontent.com/114676009/199132836-cc6b3f3a-1fa1-46d1-8e17-1d6749a3617c.png)

este codigo es un poco mas largo puesto que a cada barra es un div 
### codigo css
![imagen](https://user-images.githubusercontent.com/114676009/199132913-987d5ae3-1c64-408f-9399-d629dae22e0d.png)

# Sesion Dani
Tuve una participación activa a lo largo de la construcción del proyecto, en la conceptualización del contenido que  debía ser representado. 

###La Grafica lineal

En resumen, cada punto relaciona 1 actividad presentada en el tiempo X y relacionada con la emoción Y. Ya que trabajamos bajo el principio de que el estudiante ha calificado con una carita determinada cada actividad donde se le ha facilitado el formulario. 

En cuanto a mi sesión de la página, realicé la gráfica que brindaba una visualización de el estado de animo del estudiante por mes, era una grafica tipo lineal con dos variables: las independientes, referidas a los meses y las dependientes representadas en caras de maxima felicidad y tristeza; o intermedias de alegria o aburrimiento preocupado. Se diseñó el modelo de las caritas y se les aplicó cambio de color y movimiento en el eje x cuando se pasara el cursor por encima. 

Sobre la ejecucion. Se hizo a punta de flex box y en el interior de la grafica se usó grid. Dentro de las grillas se usó estilos de borde superior o inferior con margenes en pixeles y estilo punteado. Si se nota, este código empieza con un despliegue en columnas, que solo aplica filas en los contenidos que van entre el titulo y las variables de la horizonal, hay algunos espacios en blanco que son flex vacíos de determinada anchura. 

Cabe resaltar que las gráficas lineales son buenas para representar los cambios entonces puede ser de gran beneficio notar cuando hay un cambio abrupto de ànimo en un tiempo corto y seguido de otro totalmente distinto porque podríamos estar ante la presencia de un fenómeno positivo o negativo que sería importante averiguar por su impacto en la vida individual del estudiante y su estado mental. 



###La Grafica tortas
En cuanto a estas gráficas lo que representan es un acumulado de actividades por clase. Donde se pueden haber presentado 1 o más actividades. Lo que representan estas tortas se refiere a una única clase con muchas actividades las cuales un porcentaje el estudiante calificó en tres categorías: sentimiento de tristeza, indiferencia o felicidad. De manera que el administrador o instructor decida preocuparse por aquellas clases donde las actividades generaron en su mayoría sentimienos negativos del joven o persona en cuestion. De esta manera hay una secuencia temporal, a medida que van aumentando el número de 

La ejecución se realizó a través de flexbox y superposiciones. Los colores fueron logrados acomodando gradientes de color con grados y porcentaje de ocupación que era paralelo al diametro del circulo. En este diseño no hay animaciones. 

-----------------------------------------------------------------------------------------------------------------------------------------------------------------------

# **Nota: Cambios en el diseño de Todas las secciones** 💢💢💢

>Se obvió la realización de iconos como el de la edición en el perfil de estudiante, el de cerrar sesión y el de guardar cambios, por lo que, no se consideraron fundamentales para el cumplimiento de los requerimientos. 
Se quitó el despliegue del menú Search, ya que, no era prioritario frente a otros requerimientos que determinaban desarrollos más importantes. 

>## Gráficas 〽〽
>Las gráfica de líneas cambio por una punteada representando la misma información que se pretendía, por dificultad en el trabajo de representar una grafica así solo usando css, dado que los resultados no eran responsivos. Se intentó con triángulos formados con especificaciones de bordes de flexbox, un flex superpuesto sobre el otro, pero la visualización mostraba detalles no continuos. En cuanto al uso de transformaciones, la inclinación era constante y no funcionaba para unir las lineaas inclinadas a medida que cambiaba el tamaño de imagen. Intenté realizarlo mediante operaciones, pero incluían el width y el heigh  actual de un compartimento del grid, como no sabia si esto era posible en css y pensando en mi tasa de aprendizaje y el corto tiempo que quedaba, probar con la posibilidad de que no funcionara no era una opción. Por lo que se decidió dejar la representación expuesta. 

>## Diseño en Mobile 📱📱
>En el mobile, se decidió dejar solamente el título, la foto y el profesor, quitando solo el horario y la descripción para una mejor facilidad al hacer el scrolling.
