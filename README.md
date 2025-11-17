# Hello World – Docker (BusyBox Example)

Este repositorio contiene un ejemplo básico de Docker usando **BusyBox**. El objetivo es demostrar cómo crear una imagen personalizada copiando un archivo desde el build context y ejecutando un comando dentro del contenedor. Este es el ejercicio número 1 del taller.

## 📁 Contenido del repositorio

hello-world/
├── Dockerfile
└── hello

bash
Copy code

## 🐳 Dockerfile utilizado

```dockerfile
FROM busybox
COPY hello /hello
CMD ["cat", "/hello"]
Este Dockerfile copia el archivo hello al contenedor y al ejecutarse imprime su contenido.

🚀 Cómo ejecutar este ejercicio
Asegúrate de estar dentro de la carpeta del proyecto:

1. Construir la imagen
bash
Copy code
docker build -t helloapp:v1 .
2. Ejecutar el contenedor
bash
Copy code
docker run --rm helloapp:v1
3. Resultado esperado
Al correr el contenedor deberías ver:

nginx
Copy code
Hello World desde Docker!
