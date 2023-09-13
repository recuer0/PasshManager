Ultimate Password Manager es un administrador de contraseñas para Linux. 
Principalmente ha sido testeado en distrubuciones de Debian y Arch, pero debería poder funcionar en cualquier distribución

Es un script creado en Bash con el que podrás gestionar de manera intuitiva y segura tus contraseñas. Estas se almacenarán en tu equipo encriptadas de forma simétrica. Y la clave de encriptación estará almacenada en formato de Hash en SHA512, de forma que la
clave es irreversible.

El script cuenta con múltiples parámetros para desempeñar funciones simples como:

	1. Guardar contraseñas
 	2. Obtener una contraseña
	3. Listar los servicios guardados
 	4. Eliminar un servicio específico
	5. Cambiar la clave de encriptación
 	6. Resetear
  	7. Ver la versión de la herramienta

Algo a tener en cuenta es que cada usuario dentro del sistema tendrá sus propias contraseñas con su propia clave de encriptación, incluyendo al superusuario. Esto quiere decir que un usuario del equipo no puede ver las contraseñas de otro usuario, ya sea
mediante el uso de la herramienta o físicamente en los archivos.

El directorio raíz de almacenamiento que utiliza Ultimate Password Manager es /home/user/.config/.passwords. Aquí dentro se encuentra:

	1. Directorio decrypted --> directorio donde se almacenan temporalmente archivos de contraseñas cuando 
 	   son decriptadas para mostrarlas
 	2. Directorio encrypted --> directorio donde se almacenan los archivos de contraseñas encriptadas
	3. Archivo encryptCode  --> archivo donde se almacena el hash de la clave de encriptación
 	4. Archivo register     --> archivo donde se almacenan los servicios guardados para poder listarlos
![imagen](https://github.com/recuer0/Ultimate-PasswdM/assets/115647090/11b2cc3a-d058-4a1b-8059-5c0589612da1)

Cada vez que se ejecuta la herramienta, esta verificará la existencia de los directorios y archivos necesarios para crearlos si es necesario.
Se debe tener en cuenta que al pulsar "Ctrl + C" o abortar el programa, se realizarán una serie de comprobaciones e instrucciones para no dejar contraseñas decriptadas expuestas u otra información frágil.

Para controlar el script se podrán utilizar tanto argumentos cómo parámetros:

	-s (save)    --> Guardar una contraseña
 	-g (get)     --> Obtener una contrasñea
	-l (list)    --> Listar servicios guardados
	-d (delete)  --> Eliminar un servicio específico
 	-c (chkey)   --> Cambiar clave de encriptación
	-r (reset)   --> Resetear todo el almacenamiento
 	-v (version) --> Ver la versión de la herramienta
![imagen](https://github.com/recuer0/Ultimate-PasswdM/assets/115647090/5abcd83b-e65c-4f23-8b22-c7d5232a9333)


No recomiendo manipular los directorios y archivos en los que se almacena información, así como modificar los permisos de estos, ya que pueden suponer un riesgo de seguridad o hacer que Ultimate Password Manager no funcione debidamente.

Siempre se puede mirar el código para entender como esta herramienta funciona o para modificarlo en base a su gusto y las preferencias que tenga. El código cuenta con comentarios que le ayudarán a entender mejor este.

Es recomendable situar este script en una ruta como /bin o /usr/bin. O cualquier otra ruta incluida en el PATH, para así ejecutarla de forma relativa

Algo a tener en cuenta es que esta es mi primera herramienta y puede incluir errores, sería de gran ayuda notificarme de errores para poder subir nuevas versiones con mejoras.

Muchas Gracias!

