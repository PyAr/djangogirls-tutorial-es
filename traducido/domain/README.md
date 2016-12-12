# Dominio

PythonAnywhere te provee un dominio gratis, pero tal vez no quieres tener
".pythonanywhere.com" al final de la URL de tu blog. Tal vez quieres que tu
blog diga sólo "www.infinite-kitten-picrures.org" o
"www.3d-printed-steam-engine-parts.com" o "www.antique-buttons.com" o "www.mutant-unicornz.net" o lo que sea.

Ahora hablaremos un poco sobre dónde obtener un dominio, y cómo conectarlo con tu aplicación web en PythonAnywhere. No obstante, debes saber que la mayoría de los dominios tienen un costo monetario, y además, PythonAnywhere también cobra una cuota mensual para usar tu propio nombre de domnio -- en total no es mucho dinero, pero probablemente quieras hacerlo cuando estés realmente seguro!.
## ¿Dónde registrar un dominio?

Un dominio típico cuesta alrededor de 15 dólares estadounidenses anuales. Hay opciones más baratas y más caras, dependiendo del proveedor. Hay una gran cantidad de empresas a las que puedes comprar un dominio: una simple [búsqueda en google][1] dará cientos de opciones.

 [1]: https://www.google.com/search?q=register%20domain

Nuestra opción favorita es [I want my name][2]. Ellos se promocionan como una opción "indolora para el manejo de dominios" y realmente lo son.

 [2]: https://iwantmyname.com/

## ¿Cómo registrar un dominio en IWantMyName?

Dirígete a [iwantmyname][3] y escribe un dominio que quieras tener en el cuadro de búsqueda.

 [3]: http://iwantmyname.com

![][4]

 [4]: images/1.png

Ahora deberías ver una lista de todos los dominios disponibles con el término que pusiste en el cuadro de búsqueda. Como puedes ver, una cara sonriente indica que el dominio está disponible para comprarlo, y una cara triste indica que no se encuentra disponible.

![][5]

 [5]: images/2.png

Hemos decidido comprar `djangogirls.in`:

![][6]

 [6]: images/3.png

Dirígete a la caja. Ahora debes registrarte en iwantmyname, si todavía no tienes una cuenta. Después de eso, debes proporcionar la información de tu tarjeta de crédito y finalmente podrás comprar el dominio!

Después de eso, Haz clic en `Dominios` en el menú y elige el dominio que acabas de adquirir. A continuación, busca y da clic en el enlace de `manage DNS records`:

![][7]

 [7]: images/4.png

Ahora necesitas encontrar este formulario:

![][8]

 [8]: images/5.png

Y rellenarlo con los siguientes datos: - Hostname: www - Type: CNAME - Value: tu dominio de Heroku (por ejemplo djangogirls.herokuapp.com) - TTL: 3600

![][9]

 [9]: images/6.png

Haz click en los botones "Add" y "Save changes" en la parte inferior.

Puede tomar un par de horas para que tu dominio comience a funcionar, así que ¡sé paciente!

## Configurar dominio en Heroku

También tienes que decirle a Heroku que quieres utilizar tu dominio personalizado.

Dirígete a [Heroku Dashboard][10], inicia sesión con tu cuenta de Heroku y elije tu aplicación. Luego ve a la configuración de tu aplicación y agrega tu dominio en la sección `Domains` y guarda los cambios.

 [10]: https://dashboard.heroku.com/apps

¡Eso es todo!
