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

En el directorio **Punto-1** encontrará un archivo plantilla .yaml que contiene el código de CloudFormation con cada una de los requerimientos mencionados.

## Ejecución del Script en AWS
Una vez haya iniciado sesión en su cuenta de AWS, siga lo siguientes pasos:

1. Entrar a CloudFormation:

![Logo de la empresa](images/1.png)

2. Crear una pila:

![Logo de la empresa](images/2.png)

3. Adjuntar plantilla:

![Logo de la empresa](images/3.png)

4. Especificar los detalles de la pila:

![Logo de la empresa](images/4.png)

5. Siguiente:

![Logo de la empresa](images/5.png)

6. Validar el correcto mapeo de la configuración de la plantilla:

![Logo de la empresa](images/6.png)

7. Enviar:

![Logo de la empresa](images/7.png)

8. Actualizar la grilla y validar el estado de los eventos:

![Logo de la empresa](images/8.png)

9. Resumen de la instancia:

![Logo de la empresa](images/9.png)

10. Zona de disponibilidad:

![Logo de la empresa](images/10.png)

11. Grupo de seguridad:

![Logo de la empresa](images/11.png)

12. Clave de lanzamiento:

![Logo de la empresa](images/12.png)