1-Descargar e comprobar que unha imaxe está no teu equipo. 
Para descargar a imaxe de Ubuntu, utiliza docker pull ubuntu e verifica con docker images.

2-Crear un contenedor sen nome, queda arrincado?, cómo obtés o nome? 
Para crear un contenedor sen nome, usa docker run -d ubuntu; o contenedor queda arrincado en segundo plano e para obter o seu nome, utiliza docker ps.

3-Crea un contenedor co nome 'u1', cómo accedes a el? 
Para crear un contenedor co nome 'u1', usa docker run -d --name u1 ubuntu e para acceder a el, utiliza docker exec -it u1 bash.

4-Comproba a súa ip e fai ping a google.com. 
Comproba a súa IP con docker inspect -f '{{range .NetworkSettings.Networks}}{{.IPAddress}}{{end}}' u1 e fai ping a google.com con ping google.com.

5-Crea un contenedor co nome 'bono', pódes facer ping entre os contenedores? 
Para crear un contenedor co nome 'bono', usa docker run -d --name bono ubuntu e para comprobar se podes facer ping entre os contenedores, accede ao contenedor 'u1' e utiliza ping bono.

6-Se pechas as terminales, qué pasa co contenedor? 
Se pechas as terminales, os contenedores seguirán funcionando en segundo plano; para verificar, usa docker ps.

7-Cánta memoria no disco duro ocupaches? usa docker para calculalo. 
Para saber cantidade de memoria no disco duro ocupaches, utiliza docker system df.

8-Cánta RAM ocupan os contenedores? Crea varios para calculalo. 
Para calcular cantidade de RAM que ocupan os contenedores, hai que crear varios contenedores e usar docker stats.

9-Cómo fixeches para clonar o repositorio? 
Para clonar o repositorio, usa git clone <[](https://github.com/adrichm8/repositoriotarea1/tree/main)>.

10-Cómo engades o arquivo readme2.md? 
Para engadir o arquivo readme2.md, usa git add readme2.md.

11-Os pasos a seguir para subir o arquivo que estás editando e o arquivo readme2.md. 
Os pasos para subir o arquivo que se editan e o arquivo readme2.md son git commit -m "Engadido readme2.md" seguido de git push origin main.

12-Cómo comprobarías que existen diferencias entre o teu repositorio local e o remote? 
Para comprobar se existen diferencias entre o teu repositorio local e o remoto, usase primeiro  git fetch e despois empléase git diff origin/main.
