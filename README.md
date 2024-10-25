# Lab-sonarqube

## 1. Lo primero que hicimos fue montar el dokcer.compose.yml
```
docker-compose up -d
```
## 2. Instalar el CLI de SonarQube

[Descarga](https://docs.sonarsource.com/sonarqube/10.4/analyzing-source-code/scanners/sonarscanner/)

En este caso descargamos la version para windows. Una vez descargado se debe configurar en el path.

Agregar SonarScanner al PATH:

Sigue estos pasos:
Haz clic derecho en "Este PC" o "Mi PC" y selecciona "Propiedades".
Haz clic en "Configuración avanzada del sistema".
En la pestaña "Avanzado", haz clic en "Variables de entorno".
En "Variables del sistema", busca la variable Path y selecciona "Editar".
Agrega la ruta a la carpeta bin de SonarScanner (por ejemplo, C:\SonarScanner\bin).
Haz clic en "Aceptar" para guardar los cambios.

Verificar la instalacion
```
sonar-scanner --version
```
## 3. Iniciar sesion con el usuario por defecto

* User: admin
* Password: admin

## 4. Configurar SonarQube

![](/imgs/part1local.PNG)

![](/imgs/part2.PNG)

## 5. Correr el comando que te arroja Sonar, en este caso fue

```
sonar-scanner.bat -D"sonar.projectKey=books_manager" -D"sonar.sources=." -D"sonar.host.url=https://jubilant-acorn-gpjqppgqjgg3w769-9000.app.github.dev" -D"sonar.token=sqp_d0fa137eb571bd0b04e0d904635b3e8ffd27f2fd"
```
## 6. Revisar los logs

![](/imgs/logs.PNG)

Se crean estos archivos.

![](/imgs/files.PNG)

Tablero del projecto

![](/imgs/LogsCalDone.PNG)

