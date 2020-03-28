## Administracion de Servidores

comando
~ssh -V
~man ssh

cd ~/.ssh       si no deja entrar con ese comando, tendremos que    crear la llave ssh

crear llave
~ ssh-keygen -t rsa -b 4096 -C <correoDeGIT>
Genera llave
Pide untrar un file --- se le da enter
Pide entrar un passphrase (password): escribimos y confirmamos

cd ~/.ssh
id_rsa  -- llave completa
id_rsa.pub  -- SHA256

~nano id_rsa.pub

.pub es la llave completa
sin .pub es la llave privada


Agregar nuestra nueva llave al agent-ssh para que por default ocupe esta llave sin necesidad de ocupar la contrasenia


Meter llave al agent-ssh
~ eval "$(ssh-agent -s)"

que vaya y consulte todas las llaves que existen y las haga suya, le estamos diciendo al agente que vaya y vea que llaves estan creadas.

aniadir la llave
~ssh-add ~/.ssh/<llave a agregar>  NO PUB   ssh/ para indicar el contenido de la carpeta

Nos pedira el pass que pusimos (GIT).

las llaves se deben agregar 1 por 1



De ahi vamos a GitHub
settings
SSH
Add new SSH
ElementarySSH

copias todo el contenido de .pub (hacerle cat a la llave.pub) de color negro significa que la llave nunca ha sido utilizada.

Creamos un nuevo repo en GitHub

debe estar completamente vacio (sin el README)
