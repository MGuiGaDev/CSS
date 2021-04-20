# Glasmorphism

Contamos con 5 vídeos que practican esta estética:


## 1. [Cards Effects](https://www.youtube.com/watch?v=hv0rNxr1XXk)

### Mejores efectos

Sin duda, el primero que llama la atención es el movimiento de contenido dentro de un contenedor cuando pasamos el cursor sobre este. La aparición del contenido asociada al moviemiento del cursor es muy llamativa:

![CardHoverEffect](https://user-images.githubusercontent.com/82242888/114302980-ecfd6480-9acb-11eb-8f22-4ff553172135.gif)

### CSS

```

.container .card .content {
    padding: 20px;
    text-align: center;
    transform: translateY(100px);
    opacity: 0;
    transition: 0.5s;
}

.container .card:hover .content {
    transform: translateY(0px);
    opacity: 1;
}


```

### Dificultades

Todo funciona, pero Chrome y Firefox no reconocían la propiedad **backdrop-filter**. Buscando en la red he encontrado un artículo de [CSS-TRICKS](https://css-tricks.com/almanac/properties/b/backdrop-filter/) en el que existe una solución para esto:

```
@supports (-webkit-backdrop-filter: none) or (backdrop-filter: none) {
    .<nombreContenedor> {
    -webkit-backdrop-filter: blur(10px);
    backdrop-filter: blur(10px);
    }
    .warning {
    display: none;
    }
}
```

Esta solución es útil en Chrome, no así en Firefox.

- [ ] Debo leer este artículo pues explican en profundidaz el uso de este recurso.


## 2. [Flip Debit Card](https://www.youtube.com/watch?v=XeX1vsaufF0) 

### Mejores efectos

Si bien la disposición de los elementos dentro de **card** es para tenerla en cuenta, los dos elementos que destacan están estrechamente relacionados: la creación de dos elementos y la rotación entre los mismos.

![FlipDebitCard](https://user-images.githubusercontent.com/82242888/115343965-ef874a80-a1ac-11eb-8a95-06cfb57cc019.gif)


### CSS

```
.card:hover .face.front {
    transform: rotateY(180deg);
}
.card .face.back {
    transform: rotateY(180deg);
}
.card:hover .face.back {
    transform: rotateY(360deg);
}
```

## 3. [Glass Ussing Backdrop](https://www.youtube.com/watch?v=-2mkoKVbmGg)

### Mejores efectos

El uso de una imagen en background es reseñable, pero subrayaremos el código necesario para el movimiento de la caja acorde al movimiento del ratón.

![GlassUssingBackdrop](https://user-images.githubusercontent.com/82242888/115343843-c6ff5080-a1ac-11eb-987a-62e58f8fd8a9.gif)

### HTML

```
<section>
     <h2>MGuiGa</h2>
     <div class="glass"></div>
</section>
```
### JavaScript

```
document.addEventListener("mousemove", function(e)
        {
            const glass = document.querySelector('.glass');
            glass.style.left = e.offsetX + 'px';
            glass.style.top = e.offsetY + 'px';
        })
```

- https://www.youtube.com/watch?v=Q22Tli-D4mw
- https://www.youtube.com/watch?v=YRAoM4-Eb4A
