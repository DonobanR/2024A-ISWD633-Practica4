![image](https://github.com/DonobanR/2024A-ISWD633-Practica4/assets/135273301/976ffcbf-bce7-44dd-b83e-e86cc25fa7f8)# Limitar uso de procesador
Limitar la cantidad de núcleos de CPU:
```
--cpus=<número de núcleos>
```

Asignar núcleos de CPU específicos:
```
--cpuset-cpus=<lista de núcleos>
```

**¿Como saber el numero de procesadores virtuales que tiene una máquina?**
por medio de la siguiente liena de comanndo:

```
docker inspect --format='{{.HostConfig.CpuCount}}' server-nginx
```

solo verifica que este bien configurado tu docker:

![image](https://github.com/DonobanR/2024A-ISWD633-Practica4/assets/135273301/16309d2c-1a91-48fb-87f1-33dcd4f8564c)


## COMPLETAR

## Ejemplos
_Puedes copiar y ejecutar directamente cada uno de los comandos_

Limitar el uso de CPU a 1.5 núcleos
```
docker run -d --name server-nginx --cpus="1.5" nginx:alpine
```

Restringir el contenedor para que use los núcleos de CPU 0 a 2:
```
docker run -d --name server-nginx --cpuset-cpus="0-2" nginx:alpine
```

Restringir el contenedor para que use los núcleos de CPU 1 y 3:
```
docker run -d --name server-nginx --cpuset-cpus="1,3" nginx:alpine
```
