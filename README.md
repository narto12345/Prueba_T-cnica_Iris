# Prueba Técnica para DevOps Junior

<b>Vacante:</b> Analista Junior CloudOps
<br>
<b>Nombre del candidato:</b> Nicolás Sosa
<br>
<b>Fecha:</b> 2024-09-03
<br>
<br>
<b>Objetivo:</b> Evaluar las habilidades fundamentales en la implementación de infraestructura
como código, automatización de despliegues, y manejo de entornos en la nube.

# Requisitos

1. node.js versión 14 o superior <a href="https://nodejs.org/en">Clic</a>
2. Docker Desktop <a href="https://www.docker.com/products/docker-desktop/">Clic</a>
3. Cuenta de AWS <a href="https://aws.amazon.com/es/free/?gclid=CjwKCAjw59q2BhBOEiwAKc0ijYe6t0Ac-9NNsK7XOIIqHgjcMF_3HByJuyhmhbwj2cUgjBdEhfbQzxoCGyIQAvD_BwE&trk=8fa18207-f2c2-4587-81a1-f2a3648571b3&sc_channel=ps&ef_id=CjwKCAjw59q2BhBOEiwAKc0ijYe6t0Ac-9NNsK7XOIIqHgjcMF_3HByJuyhmhbwj2cUgjBdEhfbQzxoCGyIQAvD_BwE:G:s&s_kwcid=AL!4422!3!647999789205!e!!g!!aws!19685287144!146461596896&all-free-tier.sort-by=item.additionalFields.SortRank&all-free-tier.sort-order=asc&awsf.Free%20Tier%20Types=*all&awsf.Free%20Tier%20Categories=*all">Clic</a>

# Clonar repositorio

```cmd
mkdir laboratorio
cd laboratorio

git clone https://github.com/narto12345/Prueba_Tecnica_Iris.git

cd Prueba_Tecnica_Iris
```

# 1. Crear una instancia de EC2 en AWS:

El primer ejercicio consiste en crear una instancia de EC2 mediante CloudFormation que tenga las siguientes caracterisiticas:

- **Tipo:** t2.micro
- **Región:** us-east-1
- **OS:** Ubuntu
- clave SSH para acceso
- SSH puerto 22 solo desde nuestra IP

En el directorio **Punto-1** encontrará un fichero plantilla .yaml que contiene el código de CloudFormation con cada una de los requerimientos mencionados.

## Ejecución del Script en AWS

Una vez haya iniciado sesión en su cuenta de AWS, siga lo siguientes pasos:

1. Entrar a CloudFormation:

![imagen-1](images/1.png)

2. Crear una pila:

![imagen-2](images/2.png)

3. Adjuntar plantilla:

![imagen-3](images/3.png)

4. Especificar los detalles de la pila:

- En el parámetro **AllowedIP** digite su IP pública y seguidamente **/32** para establecer una mascara que limite la cantidad de IPs disponibles.

![imagen-4](images/4.png)

5. Siguiente:

![imagen-5](images/5.png)

6. Validar el correcto mapeo de la configuración de la plantilla:

![imagen-6](images/6.png)

7. Enviar:

![imagen-7](images/7.png)

8. Actualizar la grilla y validar el estado de los eventos:

![imagen-8](images/8.png)

9. Resumen de la instancia:

![imagen-9](images/9.png)

10. Zona de disponibilidad:

![imagen-10](images/10.png)

11. Grupo de seguridad:

![imagen-11](images/11.png)

12. Clave de lanzamiento:

![imagen-12](images/12.png)

# 2. Crear un Pipeline de CI/CD básico con GitHub Actions:

En el directorio **/.github/workflows/** encontrará un pipeline llamado **ci.yml** , el cual especeficia el siguiente comportamiento:

![pipeline](images/pipeline.png)

1. Se ejecutará cuando se haga push a la rama **main**

2. El sistema operativo sobre el que se ejecutará el job es **ubuntu-latest**

3. Obtiene el código del repositorio para que los siguientes pasos puedan trabajar con él.

4. Da permisos de ejecución al script hello.sh

5. Ejecuta el archivo **hello.sh** el cual imprime **"Hello, World!"**

6. Instala **shellcheck** para validar el código.

7. Ejecuta **shellcheck** en el script **hello.sh**

# 3. Construir y ejecutar una aplicación Docker:
