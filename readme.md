

By adding -d redis in this command, Docker will run your Redis service in “detached” mode.
Redis, therefore, runs in the background. Your container will also automatically exit when its root process exits. 
You’ll see that we’re not explicitly telling the service to “start” within this command. 
By leaving this verbiage out, our Redis service will start and continue running — remaining usable to our application.
****
https://www.docker.com/blog/how-to-use-the-redis-docker-official-image
*****
  docker run --name some-redis -p 5672:5672 -d redis
****
https://github.com/redislabs-training/node-js-crash-course
******

https://redis.io/docs/latest/develop/reference/client-side-caching/

Connect with the Redis CLI
The Redis CLI lets you run commands directly within your running Redis container. However, this isn’t automatically possible via Docker. Enter the following commands to enable this functionality: 

1
 
    docker network create some-network
1

    ​​docker run -it --network some-network --rm redis redis-cli -h some-redis
Your Redis service understands Redis CLI commands. Numerous commands are supported, as are different CLI modes. Read through the Redis CLI documentation to learn more. 

******
