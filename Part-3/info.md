# Setup

I have already register a public image in Part-2.

docker run -p 4000:80 istana/tutorialdocker:t1

Create a YAML file that defines how Docker containers should behave.

# Docker Compose file.

Usually of form `docker-compose.yml`. Here are declared the services and their configurations.

Keywords that are used in configuration:
    - image: image that is used
    - ports: list of ports that will be opened for outside of the container
    - deploy: config, number of replicas, resource usage
    - network: created network between replicas.

# Commands for the new app

docker swarm init < IOT to start the swarm mechanism

docker stack deploy -c docker-compose.yml <app-name>

docker stack ps <app-name> see all opened container of the new stack app.

## Scale

Replace with other number the replicas number from deploy option in docker-config file.

Restart app, with a new deploy

# Shut down app

docker stack rm <app-name>

This removes the app, but our one-node swarm is still up and running (as shown by docker node ls).
Take down the swarm with docker swarm leave --force.

