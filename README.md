# PROGRAMACION-WEB-SEP26-FEB27
Proyectos de la asignatura programación web
# Sitio Web de Presentación Profesional - César Vargas

## 1. Objetivo del Proyecto

Desarrollar y desplegar un sitio web de presentación profesional aplicando estándares modernos de **HTML5 semántico** y hojas de estilo en cascada (**CSS3 externo**) bajo una estética editorial moderna y responsiva, empaquetando la aplicación estática en un contenedor **Docker** servido mediante **Nginx** para garantizar portabilidad y despliegue rápido.

## 2. Tecnologías Utilizadas

* **HTML5:** Estructura semántica (`header`, `nav`, `section`, `figure`, `footer`, listas desordenadas y enlaces con logotipos).
* **CSS3 Externo:** Diseño responsivo con *CSS Grid*, *Flexbox*, variables personalizadas (`:root`), funciones fluidas (`clamp()`) y *Media Queries*.
* **Tipografía & UI:** Fuentes modernas sin serifa (`Inter`, `Segoe UI`), desplazamiento suave entre secciones (`scroll-behavior: smooth`) y tarjetas interactivas.
* **Nginx (Alpine):** Servidor web HTTP ligero de alto rendimiento.
* **Docker & Docker Hub:** Contenedorización y publicación de la imagen oficial del proyecto.
* **Git & GitHub:** Control de versiones del código fuente.

## 3. Estructura del Proyecto

```text
Perfil-Profesional/
├── estilos/
│   └── estiloperfil.css      # Hoja de estilos CSS3 externa
├── Cesar Digital.jpeg    # Fotografía de perfil profesional
├── logo-espe.png             # Logotipo institucional de la Universidad ESPE
├── logo-github.png           # Logotipo oficial de GitHub
├── index.html                # Documento principal con estructura HTML5 semántica
├── Dockerfile                # Configuración para construir la imagen con Nginx
└── README.md                 # Documentación técnica del proyecto
```

## 4. Instrucciones para Construir y Ejecutar la Imagen Docker

### Opción A: Construir y ejecutar localmente desde el repositorio

1. Clonar el repositorio:
   ```bash
   git clone [https://github.com/cesar06x/PROGRACION-WEB-SEP26-FEB27.git](https://github.com/cesar06x/PROGRACION-WEB-SEP26-FEB27.git)
   cd Perfil-Profesional
   ```

2. Construir la imagen Docker:
   ```bash
   docker build -t cesar06x/perfil-profesional:latest .
   ```

3. Ejecutar el contenedor en el puerto `8080`:
   ```bash
   docker run -d -p 8080:80 --name mi-portafolio cesar06x/perfil-profesional:latest
   ```

4. Abrir en el navegador: `http://localhost:8080`

### Opción B: Descargar y ejecutar directamente desde Docker Hub

```bash
docker pull cesar06x/perfil-profesional:latest
docker run -d -p 8080:80 --name mi-portafolio cesar06x/perfil-profesional:latest
```

## 5. Enlace a Docker Hub

* **Repositorio en Docker Hub:** [https://hub.docker.com/r/cesar06x/perfil-profesional](https://hub.docker.com/r/cesar06x/perfil-profesional)