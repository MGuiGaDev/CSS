# Glasmorphism

Contamos con 5 vídeos que practican esta estética:


## Cards Effects

- https://www.youtube.com/watch?v=hv0rNxr1XXk

Todo funciona, pero chrome y firefox no reconocían la propiedad **backdrop-filter**. Buscando en la red he encontrado un artículo de CSS-TRICKS en el que existe una solución para esto:

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

- https://www.youtube.com/watch?v=XeX1vsaufF0
- https://www.youtube.com/watch?v=-2mkoKVbmGg
- https://www.youtube.com/watch?v=Q22Tli-D4mw
- https://www.youtube.com/watch?v=YRAoM4-Eb4A
