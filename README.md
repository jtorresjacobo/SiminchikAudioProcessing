# SiminchikAudioProcessing
Processing of audio corpora for Qillqaq software
## Automatización de pruebas en el servidor
### Pre-Requisitos
* Python 2.7
* Postman
* JRE
* Node.js
### Requisitos
* Newman
* Jenkins
#### Instalación de Newman


```
sudo npm install -g newman
```


#### Instalación de Jenkins
La versión de Jenkins incluida con los paquetes predeterminados de Ubuntu a menudo está detrás de la última versión disponible del propio proyecto. Para aprovechar las últimas correcciones y características, usaremos los paquetes mantenidos por el proyecto para instalar Jenkins.
Primero, agregaremos la clave del repositorio al sistema.
```
wget -q -O - https://pkg.jenkins.io/debian/jenkins-ci.org.key | sudo apt-key add -**
```
Cuando se agrega la clave, el sistema volverá OK. A continuación, agregaremos la dirección del repositorio de paquetes de Debian a los servidores sources.list:
```
echo deb https://pkg.jenkins.io/debian-stable binary/ | sudo tee /etc/apt/sources.list.d/jenkins.list
```
Cuando ambos estén en su lugar, ejecutaremos updatepara que apt-getutilicen el nuevo repositorio:
```
sudo apt-get update
```
Finalmente, instalaremos Jenkins y sus dependencias, incluyendo Java:
```
sudo apt-get install jenkins
```
Ahora que Jenkins y sus dependencias están en su lugar, iniciaremos el servidor Jenkins.
Paso 2 - Comenzando Jenkins
Usando systemctlcomenzaremos Jenkins:
```
sudo systemctl start jenkins
```
Ya systemctlque no muestra resultados, usaremos su statuscomando para verificar que se inició correctamente:
```
sudo systemctl status jenkins
```
