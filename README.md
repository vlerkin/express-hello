## Getting Started
Clone repository with the following command:

```git clone git@github.com:vlerkin/express-hello.git```

## Running the App
To run the express app navigate to the express-hello directory you cloned and run the command:

```node app.js```

## Interacting with the App
To check if the app works open a new terminal window and run the command:

```curl http://localhost:3000/hello```

If you received output in your terminal that greets you back you are fine!

## Your Next Steps

Create a Dockerfile on the same level with the other files. Please, do not overthink, there is no need in multistage image, just a simple one is enough. 

Confused where to start?

1. Pick a base image for node.js on the DockerHub page;
2. Get back to slide 16 to ckeck out a Dockerfile example for node.js app;
3. Don't forget to expose a port so your container is not fully isolated, this port will be used by you in a curl request to talk to the app, please make the value of this port different from the port of the server, in this case it cannot be 3000 (it can but with the learning purpose let's make this port something like 5555 or another suitable number);
4. When you are finished with the Dockerfile, run [docker build command](https://docs.docker.com/reference/cli/docker/image/build/);
5. If your image built is successful, it's time to run your container, read the [documentation](https://docs.docker.com/reference/cli/docker/container/run/) to figure out how to map the port on which your server is listening to the calls and the container port you specified in the Dockerfile.
6. To check if everything works send a curl request ```curl http://localhost:YOUR_CONTAINER_PORT/hello```
