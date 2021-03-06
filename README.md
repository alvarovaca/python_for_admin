# python_for_admin

Ejercicios sobre python para administradores, para más información: [https://fp.josedomingo.org/serviciosgs/u01/python.html](https://fp.josedomingo.org/serviciosgs/u01/python.html)

## Ejercicios

Realiza un script en python que realice la siguiente función:

1. Muestra el directorio de trabajo.
2. Muestra cuantos usuarios hay definido en el sistema
3. Muestra los usuarios conectados al equipo.
4. Script que lea el nombre de un usuario, si existe dice si es administrador o no, si no existe da un mensaje de error. Realiza el script leyendo el usuario por teclado, y realiza otra versión indicándolo como parámetro.
5. Pasa por parámetros una dirección ip y un nombre de máquina e inserta en ``/etc/hosts`` (en la tercera línea) la resolución estática. Si no se introducen dos parámetros se da un error.
6. Para crear un usuario "a mano":

    * Editar ``/etc/passwd`` y agregar una nueva linea por cada nueva cuenta. Teniendo cuidado con la sintaxis. Debería hacer que el campo de la contraseña sea '*', de esta forma es imposible ingresar al sistema.
    * De forma similar, edite ``/etc/group`` para crear también un grupo.
    * Crea el directorio Inicio del usuario con el comando *mkdir*.
    * Copia los archivos de ``/etc/skel`` al nuevo directorio creado 
    * Corrige la pertenencia del dueño y permisos con los comandos *chown* y *chmod* (Ver paginas de manual de los respectivos comandos). La opción ``-R`` es muy útil. Los permisos correctos varían un poco de un sitio a otro, pero generalmente los siguientes comandos harán lo correcto:

    ```bash
    	cd /home/nuevo-nombre-de-usuario
    	chown -R nombre-de-usuario:group .
    	chmod -R 755 .
    ```
    * Asigne una contraseña con el comando *passwd*
    * Crea un script python que cree un usuario, para ello debe recibir el nombre de usuario y nombre completo por parámetros, por defecto se pone uid y gid a 2000. Mejorar el programa para que:
    * Da un error si se intenta dar de alta un usuario que ya existe
    * Al ir dando de alta a distintos usuarios vaya incrementando automáticamente el uid y el gid a partir de 2000
{% endcapture %}<div class="notice--info">{{ notice-text | markdownify }}</div>
