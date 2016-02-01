# Dominio

PythonAnywhere te provee un dominio gratis, pero tal vez no quieres tener
".pythonanywhere.com" al final de la URL de tu blog. Tal vez quieres que tu
blog diga sólo "www.infinite-kitten-picrures.org" o
"www.3d-printed-steam-engine-parts.com" o "www.antique-buttons.com" o "www.mutant-unicornz.net" o lo que sea.

Ahora hablaremos un poco sobre dónde obtener un dominio, y cómo conectarlo con tu aplicación web en PythonAnywhere. No obstante, debes saber que la mayoría de los dominios tienen un costo monetario, y además, PythonAnywhere también cobra una cuota mensual para usar tu propio nombre de domnio -- en total no es mucho dinero, pero probablemente quieras hacerlo cuando estés realmente seguro!.


## ¿Dónde registar un dominio?
A typical domain costs around $15 a year. There are cheaper and more expensive options, depending on the provider. There are a lot of companies that you can buy a domain from: a simple [google search](https://www.google.com/search?q=register%20domain) will give hundreds of options.


Nuestro favorito es [I want my name](https://iwantmyname.com/). Se promocionan
como "manejo de dominios sin dolor" y realmente es así.


## Como apuntar tu dominoio a PyhtonAnywhere

Si lo realizaste a través de *iwantmyname.com*, seleccione `Domains` en el menú
y elegir el dominio que acabas de adquirir. A continuación, busca y seleccione
el enlace `manage DNS records`.

![](images/4.png)

Ahora deber encontrar este formulario:

![](images/5.png)

Y llenarlo con los siguientes datos:
- Hostname: www
- Type: CNAME
- Value: tu dominio de PythonAnywhere (por ejemplo djangogirls.pythonanywhere.com)
- TTL: 60 

![](images/6.png)

Click the Add button and Save changes at the bottom.


> **Note** If you used a different domain provider, the exact UI for finding your DNS / CNAME settings will be different, but your objective is the same: to set up a CNAME that points your new domain at `yourusername.pythonanywhere.com`.

It can take a few minutes for your domain to start working, so be patient!


## Configure the domain via a web app on PythonAnywhere.

You also need to tell PythonAnywhere that you want to use your custom domain.

Go to the [PythonAnywhere Accounts page](https://www.pythonanywhere.com/account/) and upgrade your account. The cheapest option (a "Hacker" plan) is fine to start with, you can always upgrade it later when you get super-famous and have millions of hits.

Next, go over to the [Web tab](https://www.pythonanywhere.com/web_app_setup/) and note down a couple of things:

* Copy the **path to your virtualenv** and put it somewhere safe
* Click through to your **wsgi config file**, copy the contents, and paste them somewhere safe.

Next, **Delete** your old web app. Don't worry, this doesn't delete any of your code, it just switches off the domain at *yourusername.pythonanywhere.com*. Next, create a new web app, and follow these steps:

* Enter your new domain name
* Choose "manual configuration"
* Pick Python 3.4
* And we're done!

When you get taken back to the web tab.

* Paste in the virtualenv path you saved earlier
* Click through to the wsgi configuration file, and paste in the contents from your old config file

Hit reload web app, and you should find your site is live on its new domain!

If you run into any problems, hit the "Send feedback" link on the PythonAnywhere site, and one of their friendly admins will be there to help you in no time.

