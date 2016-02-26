# oauth

Esta es la forma insegura de obtener el access token por parte del usuario. (para ver las formas de acceder hay que [leer aquí](https://www.instagram.com/developer/authentication/).

* Dirigirse a la siguiente URL 
https://api.instagram.com/oauth/authorize/?client_id=27579ed92ccd464a8070b1de832de1ac&redirect_uri=http://localhost/&response_type=token

* Dar acceso con el usuario y contraseña.
* Autorizar la aplicación (Debe ser usuario permitido en el Sandbox).
* Es redireccionado a una URL de la siguiente forma:
http://localhost/#access_token={GRAN_NÚMERO_DE_ACCESO}
* Hay que guardar ése {GRAN_NÚMERO_DE_ACCESO}.
* Saber cuál es el user-id ingresando el usuario en http://findmyinstagramid.com/ (debe existir alguna forma de obtenerlo sin pasar por terceros. Estuve investigando, pero todos hablaban del [ACCESS TOKEN], que  no debe ser necesario porque esa página no pide autorización para dar el dato)
* Finalmente entramos a la URL
https://api.instagram.com/v1/users/{USER-ID}/followed-by?access_token={GRAN_NÚMERO_DE_ACCESO}
* Obtenemos un listado de usuarios en formato XML.
