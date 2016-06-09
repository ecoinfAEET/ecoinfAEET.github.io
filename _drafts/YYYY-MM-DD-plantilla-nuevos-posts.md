---
layout: post
title: Plantilla para escribir nuevos posts	
author: ecoinfAEET 
tags: [test, web]
---

# Título del post

Esta es una plantilla que puede utilizarse para escribir nuevas entradas o posts para la web.  [Aquí](http://ecoinfaeet.github.io/2015/04/04/publicar-contenido/) tenéis unas instrucciones detalladas de cómo contribuir.

Recuerda modificar el título, autor y etiquetas que aparecen arriba del todo (formato `YAML`).

Esto es un chunk de código:

```
df <- data.frame(x = rep(1,5, by=1),
y = rep(10,50, by=10))
```

Para incluir una imagen:

![texto]({{ site.url }}/images/nombre_del_archivo.jpg)

Todas las imágenes deben guardarse en la carpeta `images`.


Cuando el post esté terminado, guárdalo en la carpeta `_posts` con el nombre `YEAR-MONTH-DAY-title-of-the-post.md`, y haz un 'pull request' (siguiendo las instrucciones [aquí](http://ecoinfaeet.github.io/2015/04/04/publicar-contenido/)) para que aparezca publicado.






