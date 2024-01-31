# Repositorios

En sistemas basados en Red Hat, como CentOS, Fedora o Rocky Linux, la información sobre los repositorios RPM se almacena principalmente en archivos ubicados en el directorio **/etc/yum.repos.d/.** Cada archivo en este directorio representa un repositorio y contiene información sobre la ubicación del repositorio, los paquetes disponibles y otras configuraciones relevantes.

![repositorio](/img/repositorios.jpeg)

Los archivos en el directorio /etc/yum.repos.d/ son típicamente archivos de texto con la extensión .repo. Puedes abrir estos archivos con un editor de texto para ver o modificar la configuración del repositorio.

Por ejemplo, puedes encontrar un archivo de repositorio llamado **example.repo:**
```
/etc/yum.repos.d/example.repo
```
Dentro de este archivo, podrías encontrar algo similar a esto:
```
[example-repo]
name=Example Repository
baseurl=http://example.com/repo
enabled=1
gpgcheck=1
gpgkey=http://example.com/repo/RPM-GPG-KEY
```
Esto indica que hay un repositorio llamado "Example Repository" con la URL base **http://example.com/repo**, que está habilitado **(enabled=1)**, y que verifica las firmas GPG **(gpgcheck=1)** utilizando la clave GPG especificada.

Cada repositorio puede tener su propio archivo en este directorio, y estos archivos definen cómo el sistema operativo buscará e instalará paquetes RPM.
