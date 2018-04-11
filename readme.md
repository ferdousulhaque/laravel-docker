## Laravel Docker Container

Here I will Introduce you to Laravel installation setup to use Docker to create a development environment. This repo can be used as a starting point for developing Laravel apps with Docker.

This setup contains;
    <ul>
        <li>PHP-FPM (PHP 7)</li>
        <li>Nginx web server</li>
        <li>MySQL database</li>
    </ul>

## Parts of the Docker YML composing

First Step is to check the 3 Files:
    <ul>
        <li>app.docker</li>
        <li>web.docker</li>
        <li>docker-composer.yml</li>
    </ul>

Here docker-composer.yml is the orchestration file that divides the services and versions.

Each Services have the following components:

    <ul>
        <li>build: That Defines the context and dockerfile[if any]</li>
        <li>volume: That defines the volume to be used</li>
        <li>ports: That defines the ports requirement</li>
        <li>images: That defines the image reqiured</li>
        <li>environment: That defines the custom environment fields</li>
        <li>links: That defines the hierarchy</li>
    </ul>

## Clone the repo
    <pre>git clone https://github.com/ferdousulhaque/laravel-docker.git</pre>

## Change directory
<pre>cd docker-laravel</pre>

## Install dependencies

<pre>composer install
     npm install</pre>

## Build and run the Docker containers
docker-compose up -d

## Last Work
Now you are ready to check out the website from your browser: http://localhost:8080

## SSH to the docker Image
You can login to the container with the following command. First command will show the running containers. Second command will login to the container via SSH.

<pre> docker ps
      docker exec -it [container-id] bash</pre>

## Stop the Docker Container

To stop the containers run 
<pre>docker-compose kill</pre>

and to remove them run 
<pre>docker-compose rm</pre>