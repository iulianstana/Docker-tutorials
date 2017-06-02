# After dockerfile had been created and the application is written.

Build a new image from docker file.

    docker build -t friendlyHello .

    -t option for image tagging
    .  is to indicate current directory

Run app on specify port.

    docker run -p 4000:80 friendlyHello

    -p option to expose port    <port used by host machine>:<container expose port>
    -d to run in background

Use cloud.docker.com to register images.

    Create a tag for a remote image and push to cloud repository

    docker tag friendlyhello username/repository:tag
    docker push username/repository:tag

    Run cloud image on any machine

    docker run -p 4000:80 username/repository:tag

    In case I forget to specify the tag name, :latest is used.



