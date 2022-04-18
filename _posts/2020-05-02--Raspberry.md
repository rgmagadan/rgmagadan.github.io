---
Title: Experimentando con una Raspberry Pi
category: Sistemas
tags: Accesibilidad, Raspberry, Apache
summary: Cuento mi experiencia instalando y configurando una Raspberry Pi por primera vez.
---

Hace un par de días me llegó un kit de inicio para montar una Raspberry Pi, y vamos a ver sin entrar en pormenores, lo que tuve que hacer para ponerla a funcionar y el uso que le estoy dando ahora mismo, que puede que os sorprenda al final.

## ¿Por qué una Raspberry?

Últimamente he estado aprendiendo a usar Ubuntu, un sistema operativo de GNU – Linux. Lo tengo montado en una máquina virtual, y viendo que era bastante molesto estar entrando y saliendo de Windows, mi sistema anfitrión, encontré que podía conectarme por SSH y manejarlo desde la línea de comandos.

Me sonaba que SSH también se usaba para controlar la Raspberry, así que empecé a investigar y me convencí de que podía ser interesante probar una tecnología tan versátil.

## El kit de inicio

Lo que compré fue el modelo B de RaspberryPi  4, con una caja, adaptador de corriente y una tarjeta micro SD.

El montaje no puede ser más fácil. La placa solo tiene una posición dentro de la caja y el adaptador se conecta en un extremo del lateral.

## Preparando la tarjeta

Como uso la Raspberry sin pantalla, instalé Raspbian Lite en la tarjeta e incluí un archivo “ssh” dentro para habilitar desde el inicio esa conexión. Hay que recordar que para hacer esto con el ordenador se necesita lector de tarjeta.

La tarjeta se inserta luego en la Raspberry por el lado opuesto al de los USBs, en una ranura que tiene por la parte de abajo. ¡Cuidado! A mí se me cayó dentro en el primer intento.

## Conectando la Raspberry

Con esto ya podemos conectar la Raspberry al rúter y a la corriente.

Para comunicarnos con ella por SSH necesitamos saber la IP que tiene asignada. Yo lo hice con WNetWatcher. En mi caso Windows ya tiene instalado el cliente OpenSSH y solo tuve que abrir la conexión a través de la línea de comandos. La Raspberry tiene usuario y contraseña por defecto.

## ¿Y qué hago ahora con la Raspberry?

Después de cambiarle la contraseña y configurar cosas como el idioma, lo que hice pue instalar Apache, un servidor web, pero las opciones son muchísimas.

Luego abrí los puertos en el rúter para poder conectarme desde fuera de mi red, y configuré el servicio DDNS de mi administrador de dominio instalando DDClient en la Raspberry.

Para resolver el problema de la conexión segura HSTS, usé Let’s Encript con Certbot.

Perdí mucho tiempo tratando de instalar un servidor FTP y no es necesario en absoluto. Se puede usar perfectamente SFTP sin instalar ni configurar nada nuevo para enviar archivos a la Raspberry. Lo que es necesario hacer es dar permisos a tu usuario para escribir en el directorio del servidor web.

Precisamente eso es lo que voy a hacer después de escribir este artículo: copiar los archivos necesarios en la Raspberry para que tú hayas podido leer hasta aquí. Lo que significa que lo anterior ha funcionado y como quien no quiere la cosa has entrado en mi casa.

## Conclusión

El proceso de instalación y configuración de la Raspberry ha resultado ser muy accesible. La dificultad mayor ha podido venir por ser la primera vez, y de ahí la necesidad de consultar diversos manuales en Internet que usualmente se acompañan de capturas de pantalla. El presente artículo servirá por lo menos para guiar futuras instalaciones.

Solo queda disfrutar de esto mientras un *bot* no descubra mi sistema y me lo secuestre para sus fines malévolos.

Como dice un amigo: “La magia del software libre.”
