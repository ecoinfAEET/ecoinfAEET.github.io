---
layout: post
title: test how to contribute
--- 

# Instrucciones para escribir entradas. 

A continuación os indicamos unas instrucciones básicas para poder escribir entradas o posts. No obstante para cualquier duda podeís contactar con nosotros o consultar la documentación oficial de [Jekyll](https://jekyllrb.com/) 

* Las entradas o posts se generan en formato [Markdown](https://daringfireball.net/projects/markdown/) y han de tener la extensión `.md` 

* Cada entrada empieza con un trozo de código en formato YAML (`Front Matter`). Esto no es mas que unas líneas de código que especifican las características que tendrán la entrada como por ejemplo la plantilla, el título, y otra serie de variables. 
 * Utilizamos tres guiones al inicio y al final para identifcar que se trata de la información preliminar YAML 

* El nombre del archivo ha de seguir la siguiente estructura: `YEAR-MONTH-DAY-title.md` 

* Las entradas se alojarán en la carpeta `_posts`

Si queremos añadir un trozo de código podemos hacerlo del siguiente modo 


{% highlight r %}
df <- data.frame(x = rep(1,5, by=1),
				 y = rep(10,50, by=10)) 

{% endhighlight %}


