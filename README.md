# docker-nginx-assessment

### Project Description

This project creates a custom Docker image based on the official **NGINX** web server. It replaces the default NGINX welcome page with a **personalized HTML file** (`app/index.html`) containing a custom welcome message. This allows for easily deploying a simple, customized static web page inside a container.

-----

### Docker Commands

#### 1\. Build the Docker Image

Use the following command to build the Docker image. The `.` indicates that the `Dockerfile` is in the current directory, and the `-t` flag tags the image with the name `custom-nginx-webserver` and the version `1.0`.

```bash
docker build -t custom-nginx-webserver:1.0 .
```


#### 2\. Run the Docker Container

Use the following command to start a container from the built image.

  * The `-d` flag runs the container in **detached mode**.
  * The **`-p 8888:80`** flag maps the host machine's port **8888** to the container's internal NGINX port **80**.
  * The container can then be accessed by visiting `http://localhost:8888` in a web browser.

<!-- end list -->

```bash
docker run -d -p 8888:80 custom-nginx-webserver:1.0
```
