---
title: Roadmap
published: true
date: 2025-10-01 11:02
category: blog
author: Nicolas Villarroel
cover: ./images/pictures/cover-roadmap.jpg
tags:
    - hacktober2025
    - blog
---
# Roadmap 

Porque la idea de que algo funcione debe tener una definicion clara

<!---more-->

Todo tiene que empezar con algo, en el post anterior, estaba definiendo poco a poco como deberia ser este desafio y la verdad desde su origen que tiene o tendra dificultades
no tiene que ver preisamente de cosas como el no uso de IA para el sitio, tiene que ver como y donde se va a desplegar, porque hay una condicion extra que debe cumplirse (excepto por una cosa que tengo que pasar por alto)
y es el NO uso de tecnologias en la nube, tales como `AWS`, `GCP` y similares, ergo, nada de vercel, deploys utilizando CI/CD de gitlab o github (dios nos salve de Jenkins)

La excepcion seria literalmente como resolver DNS, que para este caso creo que hay que convenir en utilizar cloudflare, asi si estan leyendo esto, deben saber que esta pasando por ahi,
por supuesto eso tambien tendra su propia entrada en el blog mas pronto de lo que piensan

## A lo que vinimos

Si, el roadmap......

no es que haya mucho que decir sobre ello, solo que, tendre que poner el estado actual de el mismo en su propia pestana en el sitio, por ende tambien tiene sus propias configuraciones


asi que lo que salga en este post, puede que no sea lo que salga en la pestana cuando este vigente, ese sera mas actualizado, pero este como punto de partida esta bien


_los roadmap en si definen caminos, pero siempre las cosas tienden a diverger en el tiempo, mas si no se hacen matrices de riesgo para considerar y en este caso no hare una_


### Tareas

las tareas a realizar son:

- Crear estructura base de blog
- SEO
- Dejar el contenido del blog en un repositorio aparte
- Instalar libreria UI gratuita
- Configurar que las imagenes del contenido del blog sean desde el repositorio de posts y no desde el blog en si (se expliara en su momento)
- Actualizar, readme base, editorconfig, prettier, eslint, etc en ambos repos 
- Crear los registros DNS
- crear repositorio de arquitectura de Todo
- habilitar actualizacion automatica en servicio que tendra desplegado el sitio
- configurar respaldos (opcional, pero recomendado)
- documentar

la idea es que en la seccion [Roadmap](/roadmap) puedan ver un kanban (si, aunque moleste) de las cosas que se estan realizando y las pendientes, actualizarlo como buena practica

no he puesto un listado de posts, porque si bien hay varios programados, tengo varios que realizar en el camino y el como los vaya habilitando es algo que quiero controlar, como contenido, no como una bitacora

eventualmente habra algo parecido a una bitacora y la idea es que esto crezca en el tiempo, no solo este desafio, por eso tambien tantas condiciones, para que despues esto sea una plataforma tambien.


