# repositoriotarea1
1. Descargar y comprobar la imagen
Primero, necesitas descargar la imagen de Ubuntu para poder crear contenedores basados en ella.

Comando: docker pull ubuntu
Para verificar que la imagen se ha descargado correctamente, utiliza:
Comando: docker images
2. Crear un contenedor sin nombre
Puedes crear un contenedor en segundo plano sin asignarle un nombre específico, lo que te permitirá ejecutarlo sin necesidad de identificarlo por nombre.

Comando: docker run -d ubuntu
Para comprobar que el contenedor se está ejecutando, utiliza:
Comando: docker ps
3. Crear un contenedor llamado 'u1'
Ahora, puedes crear un contenedor al que le asignarás un nombre específico, facilitando su gestión.

Comando: docker run -d --name u1 ubuntu
Para acceder al contenedor y trabajar dentro de él, usa:
Comando: docker exec -it u1 bash
4. Comprobar IP y hacer ping
Es útil conocer la dirección IP del contenedor para establecer comunicaciones entre contenedores o con el exterior.

Comando para comprobar IP: docker inspect -f '{{range .NetworkSettings.Networks}}{{.IPAddress}}{{end}}' u1
Luego, puedes hacer un ping a google.com para verificar la conectividad:
Comando: ping google.com
5. Crear un contenedor llamado 'bono'
Similar al contenedor 'u1', puedes crear otro contenedor con un nombre específico.

Comando: docker run -d --name bono ubuntu
Para verificar la conectividad entre contenedores, accede a uno de ellos y usa:
Comando: ping bono
6. Cierre de terminales
Si cierras las terminales, los contenedores seguirán funcionando en segundo plano, lo que significa que no se detendrán.

Para verificar su estado, ejecuta:
Comando: docker ps
7. Espacio en disco ocupado
Es importante conocer cuánto espacio en disco están utilizando tus imágenes y contenedores.

Comando: docker system df para obtener un resumen del uso de disco.
8. Uso de RAM
Para supervisar el uso de memoria RAM de los contenedores en funcionamiento, puedes utilizar:

Comando: docker stats, que te mostrará el uso de recursos en tiempo real.
9. Clonar el repositorio
Clonar un repositorio te permite obtener una copia local del mismo para trabajar en él.

Comando: git clone <URL-del-repositorio> (reemplaza <URL-del-repositorio> por la dirección de tu repositorio).
10. Añadir readme2.md
Crear un archivo readme2.md te permite agregar información adicional sobre tu proyecto.

Comando: echo "Tu frase aquí" > readme2.md (cambia "Tu frase aquí" por el contenido que desees).
11. Subir cambios
Para enviar tus cambios al repositorio remoto, primero debes añadir los archivos modificados y luego realizar un commit.

Comando para añadir archivos: git add readme.md readme2.md
Comando para hacer commit: git commit -m "Añadido readme2.md y actualizaciones en readme.md"
Comando para subir: git push origin main
12. Comprobar diferencias
Es útil comprobar si hay diferencias entre tu repositorio local y el remoto antes de subir cambios.

Comando: git fetch para obtener información sobre el remoto.
Para ver las diferencias, utiliza:
Comando: git diff origin/main
