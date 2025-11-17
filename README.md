# Hello World – Docker (BusyBox Example)

Este repositorio contiene un ejemplo básico de Docker usando **BusyBox**. El objetivo es demostrar cómo crear una imagen personalizada copiando un archivo desde el build context y ejecutando un comando dentro del contenedor. Este es el ejercicio número 1 del taller.


El archivo `hello` contiene el texto que será mostrado al ejecutar el contenedor.

---

##  Dockerfile

```dockerfile
FROM busybox
COPY hello /hello
CMD ["cat", "/hello"]
```
##  Construir la imagen
```bash
docker build -t helloapp:v1 .
```
##  Ejecucion del contenedor
```bash
docker run --rm helloapp:v1
```
