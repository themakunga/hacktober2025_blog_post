---
title: On Premise
published: false
date: 2025-10-02 23:02
category: blog
author: Nicolas Villarroel
cover: ./images/pictures/cover-onpremise.jpg
tags:
  - hacktober2025
  - blog
  - tutorial
---
# {{$doc.title}}

Se podria decir que este es el primer post, por lo que hay que explicar tambien un par de cosas, como por ejemplo en que arquitectura se esta sosteniendo?

<!--more-->

Si bien seria contra producente revelar en que estas hosteando tus servicios, el ejercicio de este desafio tambien considera la arquitectura, por lo que estar ocultando todo seria bastante raro.

primero que todo a modo de Q/A :

## Que nube estoy usando?

la respuesta, ninguna, todo se esta realizando de manera on-premise, graciosamente es una `raspberry pi 5` con un disco NVME que tenia en casa sin hacer nada, estoy utilizando tuneles de cloudflare para exponer los servicios especificos a internet y utilizando coolify para poder gestionar todo 

todo esto siendo mantenido con open tofu

en resumen en hardware
- Raspberry pi5 16gb de ram + nvme hat con un ssd de 512Gb
- cables de red cat 5e 
- un switch gigabit que realmente no se el modelo
- el router de mi proveedor de internet en casa sin ningun puerto abierto a publico (el tipico con ip dinamica)

en software
- SO, debian linux
- Coolify 
- Docker / docker-compose usando Colima 
- Nix como gestor de paquetes
- Opentofu como IaC (infrastructure as Code)
- contenedores, contenedores y mas contenedores para gestionar los servicios que necesito

---

No pasare por cada cosa y como instalarla, menos ire a mostrar los archivos de flakes que uso en nix en mi servidor, pero no es nada del otro mundo, nada que un buen flake que ya exista y agregarle como `environment.pkgs` los servicios escenciales que necesito.

la idea de usar una herramienta como **coolify** es emular el como seria tener una solucion cloud como `AWS` o `GCP` sin tener que depender de esas empresas que tienden a secuestrar tu trabajo si no tienes como pagar sus inexplicables facturas.

## El dilema del huevo y la gallina...

uno de los principales problemas al utilizar `opentofu` es como manejas los state del servicio 

:::Alert{type="info"}
  opentofu es literamente el heredero open source de `terraform`, tienen la misma sintaxis y la linea de comandos funciona casi de la misma manera, incluso las dependencias o providers, son los mismos que usa actualmente `terraform`, tuvieron una diferencia en el cambio de licencia de `terraform`
  asi que este fork viene a usar el espacio de la gente que rehusa a utilizar otras herramientas de IaC como `pulumi`, `cloudformation`, `CDK` y `troposphere`.
:::


