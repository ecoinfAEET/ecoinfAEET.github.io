---
layout: post
title: Publicar Contenido
author: ecoinfAEET
tags: [web, github, compartir datos]
--- 

# Instrucciones para escribir entradas. 
Esta web está está creada con [Jekyll](https://jekyllrb.com/), un generador de sitios web (con estilo blog) muy sencillo. Partiendo de una serie de plantillas convierte archivos de texto plano (con algunas especificaciones) en entradas de una web. 

Jekyll es el motor que ha detrás de las páginas de GitHub, por lo que se puede utilizar para acoger sitios webs, blogs o páginas de cursos alojándolos directamente en GitHub de una forma gratuita. 

# Acceso al repositorio 
El primer paso para poder aportar contenido es crear un **fork** del [repositorio](https://github.com/ecoinfAEET/ecoinfAEET.github.io). Se trata de una copia del repositorio en tu cuenta de github. 

Posteriormente es necesario **clonar** tu fork en tu equipo. Para ello has de teclear el siguiente comando: 

{% highlight text %}
git clone git@github.com:usuario/ecoinfAEET.github.io.git
{% endhighlight %} 

sustituyendo `usuario` por tu usuario de github. Con esto obtendrás una copia local (clone) de tu fork. 

Una vez que hayas hecho las aportaciones (con los commits correspondientes) de tus cambios en el repositorio local, es necesario actualizar tu repositorio remoto. Para ello utilizas el comando: 

{% highlight text %}
git push origin master
{% endhighlight %} 

Finalmente es necesario realizar un **pull request** al repositorio oficial del proyecto. Se trata de una operación que añade tus contribuciones al repositorio oficial. Para ello es necesario clickar al icono que aparece en la página oficial de tu repositorio remoto en el lado derecho que dice: `Pull Request y luego hacer clic en `New pull request`. Es necesario seleccionar el branch del repositorio oficial donde quieres agregar tus contribuciones (en este caso es el `master`) y el branch donde están tus cambios reaizados. 

De esta forma se ha generado la solicitud para integrar tu contenido en el repositorio del grupo de trabajo de Ecoinformática de la AEET. Y lo último sería esperar a que alguno de los administradores revisen los cambios realizados y acepten la solicitud. 

# ¿Cómo escribir entradas? 
A continuación os indicamos unas instrucciones básicas para poder escribir entradas o posts. Para cualquier duda podéis consultar la documentación oficial de [Jekyll](https://jekyllrb.com/docs/home/) o contactar con nosotros [ecoinf.aeet@gmail.com](mailto:ecoinf.aeet@gmail.com). 

* Las entradas o posts se generan en formato [Markdown](https://daringfireball.net/projects/markdown/) y han de tener la extensión `.md` 

* Cada entrada empieza con un trozo de código donde se especifican las características que tendrá la entrada, como por ejemplo la plantilla, el título, y otra serie de variables.

* El **nombre del archivo** ha de seguir la siguiente estructura: `YEAR-MONTH-DAY-title.md` 

* Las entradas se alojarán en la carpeta `_posts`

## Encabezado en cada entrada
Al inicio de cada entrada hemos de especificar algunas variables de configuración en formato YAML (`Front Matter`). Se trata de un bloque de código delimitado por tres guiones (`---`).

* **layout**: tipo de plantilla que utilizaremos en la entrada. Por defecto utilizaremos el valor `post` 
* **title**: Título de la entrada
* **author**: Autor de la entrada
* **tags**: etiquetas de la entrada. Valores separados por `,` dentro de corchetes. Por ejemplo: `[etiqueta1, etiqueta 2]` 

El campo `author` identifica la persona que escribe la entrada. Para ello antes de escribir una entrada es necesario dar de alta un autor en la lista de contribuidores del grupo de trabajo. Contacta con los [administradores](mailto:ecoinf.aeet@gmail.com) para darte de alta como contribuidor. 

Un ejemplo del encabezado sería: 

{% highlight text %}
{% raw %}{% highlight r %}{% endraw %}
---
layout: post
title: Manipular datos en R
author: ecoinfAEET
tags: [R, compartir datos, ciencia reproducible]
--- 
{% raw %}{% endhighlight %}{% endraw %} 
{% endhighlight %}
 
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

