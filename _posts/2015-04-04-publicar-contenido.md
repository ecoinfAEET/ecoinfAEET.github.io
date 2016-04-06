---
layout: post
title: Publicar Contenido
author: antonioj_perez, sara_varela
tags: [web, github, compartir datos]
--- 

# Instrucciones para escribir entradas. 
Esta web está está creada con [Jekyll](https://jekyllrb.com/), un generador de sitios web (con estilo blog) muy sencillo. Partiendo de una serie de plantillas convierte archivos de texto plano (con algunas especificaciones) en entradas de una web. 

Jekyll es el motor que ha detrás de las páginas de GitHub, por lo que se puede utilizar para acoger sitios webs, blogs o páginas de cursos alojándolos directamente en GitHub de una forma gratuita. 

# ¿Cómo escribir entradas? 
A continuación os indicamos unas instrucciones básicas para poder escribir entradas o posts. Para cualquier duda podeís consultar la documentación oficial de [Jekyll](https://jekyllrb.com/docs/home/) o contactar con nosotros [ecoinf.aeet@gmail.com](mailto:ecoinf.aeet@gmail.com). 

* Las entradas o posts se generan en formato [Markdown](https://daringfireball.net/projects/markdown/) y han de tener la extensión `.md` 

* Cada entrada empieza con un trozo de código en formato YAML (`Front Matter`). Se trata de unas líneas de código que especifican las características que tendrá la entrada, como por ejemplo la plantilla, el título, y otra serie de variables. 
 * Utilizamos tres guiones al inicio y al final para identifcar que se trata de la información preliminar YAML 

* El **nombre del archivo** ha de seguir la siguiente estructura: `YEAR-MONTH-DAY-title.md` 

* Las entradas se alojarán en la carpeta `_posts`

## Añadir elementos a nuestra entrada

### Código 
Si queremos añadir un trozo de código podemos hacerlo del siguiente modo. Hemos de incluir el código entre dos líneas especiales: 

Por ejemplo si escribimos 

{% highlight text %}
{% raw %}{% highlight r %}{% endraw %}
df <- data.frame(x = rep(1,5, by=1),
y = rep(10,50, by=10))
{% raw %}{% endhighlight %}{% endraw %} 
{% endhighlight %}

aparecerá 

{% highlight r %}
df <- data.frame(x = rep(1,5, by=1),
y = rep(10,50, by=10)) 
{% endhighlight %} 

### Imágenes 
* Todas las imágenes tiene que estar alojadas dentro la carpeta `/images/` 
* Las sintáxis para incluir una imagen en una entrada es similar a la utilizada por Markdown, con una pequeña modificación. Así escribiremos:  


{% highlight text %}
![texto]({% raw %}{{ site.url }}{% endraw %}/images/nombre_del_archivo.jpg)
{% endhighlight %}

Por ejemplo para incluir la imagen `ecoinf_10.jpg` el código sería: 

{% highlight text %}
![logo]({% raw %}{{ site.url }}{% endraw %}/images/logo/ecoinf_10.jpg)
{% endhighlight %}

![logo](http://ecoinfAEET.github.io/images/logo/ecoinf_10.jpg)

