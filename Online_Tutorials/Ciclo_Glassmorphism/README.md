# Glasmorphism

Contamos con 5 vídeos que practican esta estética:


## 1. Cards Effects

- https://www.youtube.com/watch?v=hv0rNxr1XXk

### Mejores efectos

Sin duda, el primero que llama la atención es el movimiento de contenido dentro de un contenedor cuando pasamos el cursor sobre este. La aparición del contenido asociada al moviemiento del cursor es muy llamativa:

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



- https://www.youtube.com/watch?v=XeX1vsaufF0
- https://www.youtube.com/watch?v=-2mkoKVbmGg
- https://www.youtube.com/watch?v=Q22Tli-D4mw
- https://www.youtube.com/watch?v=YRAoM4-Eb4A
