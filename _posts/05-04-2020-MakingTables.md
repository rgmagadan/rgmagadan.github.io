
---
layout: postTitle: Generando tablas en Markdown con Python
Date: 2020-04-05 12:33
Category: Productividad
Tags: Python, Markdown, Programación, Excel
Authors: Ramón García
Summary: Enseñando una herramienta para generar tablas fácilmente con Markdown usando Python
---

A continuación comento brevemente un pequeño script escrito en Python, que toma el contenido del portapapeles, lo formatea con Markdown y lo escribe en cualquier documento. Al final dejaré el enlace al repositorio que contiene el archivo.

## La combinación Python con Markdown

Aunque Markdown es un código muy sencillo para dar formato a un documento, la construcción de tablas es algo tedioso, sobre todo cuando tenemos herramientas para eso tan buenas como Excel o cualquier hoja de cálculo. Tal vez algún editor haya resuelto el problema, pero yo no uso ninguno específico.

Como me pasa siempre que no encuentro una manera satisfactoria de hacer algo con el ordenador, después de darle unas vueltas, acabo por convencerme de que Python puede ser la solución. Y en mi caso, disfruto tanto desarrollando la idea como con el problema resuelto.

## Desarrollando la idea

Empecé usando Excel para hacer las tablas. Luego sustituía los tabuladores por las barras verticales y así me arreglaba. Hasta que encontré que la librería Pandas tiene un método para tomar el contenido del portapapeles y generar un *dataframe*. Sabiendo que Python provee de librerías para Markdown, ya sospechaba que lo tenía resuelto… y encontré que también Pandas tenía otro método para formatear el *dataframe* con Mardown.

Con eso realmente ya estaba, porque podía escribir el resultado en un archivo de texto, pero si Python lo puede escribir directamente en el documento que estoy editando, ¡Mucho mejor! Esto lo conseguí con la librería Pynput.

Además de Pandas y Pynput se necesita un último módulo que se puede instalar con *pip*, pero que no es necesario importar en el script porque Pandas se encarga de eso. El módulo es *Tabulate*.

Al principio intenté llamar al script desde el documento con un atajo de teclado, pero el foco se movía y el texto no se escribía. La solución más fácil para esto fue dormir el proceso un par de segundos para que me diera tiempo a situarme en el documento después de abrir el programa.

## Uso del script

Si has llegado hasta aquí, lo que sigue es trivial, pero no está de más.

1. Escribe la tabla en una hoja de cálculo (no es necesario darle formato de tabla).
2. Copia dicha tabla.
3. Ejecuta el script y sitúa el foco rápidamente en el documento Markdown.

Si todo ha ido bien, verás la tabla formateada en la posición del cursor.

Puedes descargarte el programa de su [repositorio en GitHub.](https://github.com/rgmagadan/MakingTables)

