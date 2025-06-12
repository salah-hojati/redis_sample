

By adding -d redis in this command, Docker will run your Redis service in “detached” mode.
Redis, therefore, runs in the background. Your container will also automatically exit when its root process exits. 
You’ll see that we’re not explicitly telling the service to “start” within this command. 
By leaving this verbiage out, our Redis service will start and continue running — remaining usable to our application.

https://www.docker.com/blog/how-to-use-the-redis-docker-official-image

docker run --name some-redis -p 5672:5672 -d redis

https://github.com/redislabs-training/node-js-crash-course
