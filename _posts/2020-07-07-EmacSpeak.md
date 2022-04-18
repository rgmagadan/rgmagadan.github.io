---
title: Lector de pantalla en la Raspberry con EmacSpeak
category: Raspberry
tags: EmacSpeak, Raspberry, lector de pantalla
summary: Cuento cómo he hecho que hable la Rasperry usando EmacSpeak, un editor de texto con lector de pantalla.
---

Estaba tan  contento utilizando la Raspberry como servidor, manejándola a través de *ssh*, hasta que empecé a pensar que además también podría usarla directamente conectándole un teclado e instalándole un lector de pantalla.

## Lector de pantalla para la Raspberry

Al parecer hay varias alternativas, con y sin entorno gráfico. Con entorno gráfico está el conocido Orca, para el que la Raspberry ya tiene soporte, aunque yo no supe hacerlo funcionar; y sin entorno gráfico, estuve intentando instalar Fenrir, con el mismo éxito. Por otra parte, sabía de EmacSpeak, pero me resistía a usarlo porque en principio me parecía que no tenía necesidad de añadir más complejidad al asunto. Quería un lector para la línea de comandos y ya...

Por el camino aprendí algunas cosas interesantes, como  que a la Rasperry se le puede dar una configuración wifi de inicio o que a través de raspi-config se puede configurar el acceso por consola sin *login*.

## EmacSpeak

Frustrado ya de tanto esfuerzo inútil, después de haber instalado EmacSpeak, con unos auriculares y un teclado conectados a la Raspberry. Simplemente hice: “emacspeak” (sin comillas), y empecé a escuchar una voz muy lenta y en inglés, pero me sonó divina. Buceando un poco por la web, encontré algunos comandos útiles:

- C-e d S (S mayúscula), luego "es" (sin comillas) y "Enter"; para poner la voz en español.
- C-e d p, y seleccionar con flechas la puntuación.
- C-e d r, escribir número de palabras por minuto y "Enter", para seleccionar la velocidad del habla.

Ahora estoy aprendiendo a usar EmacSpeak y me estoy convenciendo de que esta debió ser siempre la primera opción, porque me permite hacer cosas increíbles, como tener abierto un archivo, una terminal Linux y otra Python, por ejemplo, todo en la misma pantalla, y en remoto, si lo necesito.

No es fácil. El tutorial que se puede leer en español desde la página inicial del programa, ayuda bastante al principio.

Y si lo hemos abierto, ahora habrá que cerrarlo:

C-x C-c.