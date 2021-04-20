# Full page slider

De esta práctica, debo destacar un elemento de valor: el uso de JavaScript para el funcionamiento del Slide.

![FullPageSlide](https://user-images.githubusercontent.com/82242888/115339803-c4e5c380-a1a5-11eb-82d4-b6f31f701d22.gif)


Contamos con 4 imágenes y 4 cajas de descripción que funcionan al unísono con el slide. Veremos el ejemplo con el código usado para las imágenes y los controles del slide:

## HTML:

```
 <div class="imgBx">
      <img src="imagenes/img1.jpg" alt="" class="active">
      <img src="imagenes/img2.jpg" alt="">
      <img src="imagenes/img3.jpg" alt="">
      <img src="imagenes/img4.jpg" alt="">
</div>
```

```
<ul class="controls">
      <li onclick="prevSlide();prevSlideText();"></li>
      <li onclick="nextSlide();nextSlideText();"></li>
</ul>
```
## JAVASCRIPT

```
        const imgBx = document.querySelector('.imgBx');
        const slides = imgBx.getElementsByTagName('img');
        var i = 0;

        function nextSlide(){
            slides[i].classList.remove('active');
            i = (i + 1) % slides.length;
            slides[i].classList.add('active');
        }
        function prevSlide(){
            slides[i].classList.remove('active');
            i = (i - 1 + slides.length) % slides.length;
            slides[i].classList.add('active');
        }
```




