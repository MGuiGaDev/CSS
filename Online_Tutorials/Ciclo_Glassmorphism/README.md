# Glasmorphism

Contamos con 5 vídeos que practican esta estética:


## 1. Cards Effects

- https://www.youtube.com/watch?v=hv0rNxr1XXk

### Mejores efectos

Sin duda, el primero que llama la atención es el movimiento de contenido dentro de un contenedor cuando pasamos el cursor sobre este. La aparición del contenido asociada al moviemiento del cursor es muy llamativa:

![CardHoverEffect](https://user-images.githubusercontent.com/82242888/114302980-ecfd6480-9acb-11eb-8f22-4ff553172135.gif)


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


## 2. Flip Debit Card 

- https://www.youtube.com/watch?v=XeX1vsaufF0


![FlipDebitCard](https://user-images.githubusercontent.com/82242888/115343965-ef874a80-a1ac-11eb-8a95-06cfb57cc019.gif)




## 3. Glass Ussing Backdrop

![GlassUssingBackdrop](https://user-images.githubusercontent.com/82242888/115343843-c6ff5080-a1ac-11eb-987a-62e58f8fd8a9.gif)![Uploading FlipDebitCard.gif…]()

- https://www.youtube.com/watch?v=-2mkoKVbmGg
- https://www.youtube.com/watch?v=Q22Tli-D4mw
- https://www.youtube.com/watch?v=YRAoM4-Eb4A
