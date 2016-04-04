---
layout: post
title: test how to contribute
--- 

# Instrucciones para escribir entradas. 
Esta web está está creada con [Jekyll](https://jekyllrb.com/), que es un generador de web (con estilo blog) muy sencillo. Partiendo de una serie de plantillas convierte archivos de texto plano (con algunas especificaciones) en entradas de una web. 

Jekyll es el motor que ha detrás de las páginas de GitHub, por lo que se puede utilizar para acoger sitios webs, blogs o páginas de cursos alojándolos directamente en GitHub de una forma gratuita. 

# ¿Cómo escribir entradas? 
A continuación os indicamos unas instrucciones básicas para poder escribir entradas o posts. Para cualquier duda podeís consultar la documentación oficial de [Jekyll](https://jekyllrb.com/docs/home/) o contactar con nosotros [ecoinf.aeet@gmail.com](mailto:ecoinf.aeet@gmail.com). 
 
* Las entradas o posts se generan en formato [Markdown](https://daringfireball.net/projects/markdown/) y han de tener la extensión `.md` 

* Cada entrada empieza con un trozo de código en formato YAML (`Front Matter`). Esto no es mas que unas líneas de código que especifican las características que tendrán la entrada como por ejemplo la plantilla, el título, y otra serie de variables. 
 * Utilizamos tres guiones al inicio y al final para identifcar que se trata de la información preliminar YAML 

* El nombre del archivo ha de seguir la siguiente estructura: `YEAR-MONTH-DAY-title.md` 

* Las entradas se alojarán en la carpeta `_posts`

Si queremos añadir un trozo de código podemos hacerlo del siguiente modo. Hemos de incluir el código entre dos líneas especiales: 

* inicio: {% highlight r %}
* fin: {% endhighlight %} 

Por ejemplo si escribimos 

```
{% highlight r %}
df <- data.frame(x = rep(1,5, by=1),
y = rep(10,50, by=10)) 
{% endhighlight %}
```

aparecerá 

{% highlight r %}
df <- data.frame(x = rep(1,5, by=1),
y = rep(10,50, by=10)) 
{% endhighlight %} 
