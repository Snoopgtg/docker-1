## How to Docker
  1. Create a virtual machine with docker-machine using the virtualbox driver, and named Char.
 <a href="https://github.com/Snoopgtg/docker-1/blob/master/00_how_to_docker/01" target="blank">01</a>
 
 2. Get the IP address of the Char virtual machine.
<a href="https://github.com/Snoopgtg/docker-1/blob/master/00_how_to_docker/02" target="blank">02</a>

3. Define the variables needed by your virtual machine Char in the general env of your
terminal, so that you can run the docker ps command without errors. You have
to fix all four environment variables with one command, and you are not allowed
to use your shell’s builtin to set these variables by hand.
<a href="https://github.com/Snoopgtg/docker-1/blob/master/00_how_to_docker/03" target="blank">03</a>

4. Get the hello-world container from the Docker Hub, where it’s available.
<a href="https://github.com/Snoopgtg/docker-1/blob/master/00_how_to_docker/04" target="blank">04</a>

5. Launch the hello-world container, and make sure that it prints its welcome message,
then leaves it.
<a href="https://github.com/Snoopgtg/docker-1/blob/master/00_how_to_docker/05" target="blank">05</a>

6. Launch an nginx container, available on Docker Hub, as a background task. It
should be named overlord, be able to restart on its own, and have its 80 port
attached to the 5000 port of Char. You can check that your container functions
properly by visiting
http://<ip-de-char>:5000 on your web browser.
<a href="https://github.com/Snoopgtg/docker-1/blob/master/00_how_to_docker/06" target="blank">06</a>

7. Get the internal IP address of the overlord container without starting its shell and
in one command.
<a href="https://github.com/Snoopgtg/docker-1/blob/master/00_how_to_docker/07" target="blank">07</a>

8. Launch a shell from an alpine container, and make sure that you can interact
directly with the container via your terminal, and that the container deletes itself
once the shell’s execution is done.
<a href="https://github.com/Snoopgtg/docker-1/blob/master/00_how_to_docker/08" target="blank">08</a>

9. From the shell of a debian container, install via the container’s package manager
everything you need to compile C source code and push it onto a git repo (of
course, make sure before that the package manager and the packages already in the
container are updated). For this exercise, you should only specify the commands
to be run directly in the container.
<a href="https://github.com/Snoopgtg/docker-1/blob/master/00_how_to_docker/09" target="blank">09</a>

10. Create a volume named hatchery.
<a href="https://github.com/Snoopgtg/docker-1/blob/master/00_how_to_docker/10" target="blank">10</a>

11. List all the Docker volumes created on the machine. Remember. VOLUMES. 
<a href="https://github.com/Snoopgtg/docker-1/blob/master/00_how_to_docker/11" target="blank">11</a>

12. Launch a mysql container as a background task. It should be able to restart on its
own in case of error, and the root password of the database should be Kerrigan.
You will also make sure that the database is stored in the hatchery volume, that
the container directly creates a database named zerglings, and that the container
itself is named spawning-pool.
<a href="https://github.com/Snoopgtg/docker-1/blob/master/00_how_to_docker/12" target="blank">12</a>

13. Print the environment variables of the spawning-pool container in one command,
to be sure that you have configured your container properly.
<a href="https://github.com/Snoopgtg/docker-1/blob/master/00_how_to_docker/13" target="blank">13</a>

14. Launch a wordpress container as a background task, just for fun. The container
should be named lair, its 80 port should be bound to the 8080 port of the virtual
machine, and it should be able to use the spawning-pool container as a database
service. You can try to access lair on your machine via a web browser, with the
IP address of the virtual machine as a URL.
Congratulations, you just deployed a functional Wordpress website in two commands!
<a href="https://github.com/Snoopgtg/docker-1/blob/master/00_how_to_docker/14" target="blank">14</a>

15. Launch a phpmyadmin container as a background task. It should be named roach-warden,
its 80 port should be bound to the 8081 port of the virtual machine and it should
be able to explore the database stored in the spawning-pool container.
<a href="https://github.com/Snoopgtg/docker-1/blob/master/00_how_to_docker/15" target="blank">15</a>

16. Look up the spawning-pool container’s logs in real time without running its shell.
<a href="https://github.com/Snoopgtg/docker-1/blob/master/00_how_to_docker/16" target="blank">16</a>

17. Display all the currently active containers on the Char virtual machine.
<a href="https://github.com/Snoopgtg/docker-1/blob/master/00_how_to_docker/17" target="blank">17</a>

18. Relaunch the overlord container.
<a href="https://github.com/Snoopgtg/docker-1/blob/master/00_how_to_docker/18" target="blank">18</a>

19. Launch a container name Abathur. It will be a Python container, 2-slim version,
its /root folder will be bound to a HOME folder on your host, and its 3000 port
will be bound to the 3000 port of your virtual machine.
You will personalize this container so that you can use the Flask micro-framework
in its latest version. You will make sure that an html page displaying "Hello World"
with `<h1>` tags can be served by Flask. You will test that your container is
properly set up by accessing, via curl or a web browser, the IP address of your
virtual machine on the 3000 port.
You will also list all the necessary commands in your repository.
<a href="https://github.com/Snoopgtg/docker-1/blob/master/00_how_to_docker/19" target="blank">19</a>

20. Create a local swarm, the Char virtual machine should be its manager.
<a href="https://github.com/Snoopgtg/docker-1/blob/master/00_how_to_docker/20" target="blank">20</a>

21. Create another virtual machine with docker-machine using the virtualbox driver,
and name it Aiur.
<a href="https://github.com/Snoopgtg/docker-1/blob/master/00_how_to_docker/21" target="blank">21</a>

22. Turn Aiur into a slave of the local swarm in which Char is leader (the command to
take control of Aiur is not requested).
<a href="https://github.com/Snoopgtg/docker-1/blob/master/00_how_to_docker/22" target="blank">22</a>

23. Create an overlay-type internal network that you will name overmind.
<a href="https://github.com/Snoopgtg/docker-1/blob/master/00_how_to_docker/23" target="blank">23</a>

24. Launch a rabbitmq SERVICE that will be named orbital-command. You should
define a specific user and password for the RabbitMQ service, they can be whatever
you want. This service will be on the overmind network.
<a href="https://github.com/Snoopgtg/docker-1/blob/master/00_how_to_docker/24" target="blank">24</a>

25. List all the services of the local swarm.
<a href="https://github.com/Snoopgtg/docker-1/blob/master/00_how_to_docker/25" target="blank">25</a>

26. Launch a 42school/engineering-bay service in two replicas and make sure that
the service works properly (see the documentation provided at hub.docker.com).
This service will be named engineering-bay and will be on the overmind network.
<a href="https://github.com/Snoopgtg/docker-1/blob/master/00_how_to_docker/26" target="blank">26</a>

27. Get the real-time logs of one the tasks of the engineering-bay service.
<a href="https://github.com/Snoopgtg/docker-1/blob/master/00_how_to_docker/27" target="blank">27</a>

28. ... Damn it, a group of zergs is attacking orbital-command, and shutting down
the engineering-bay service won’t help at all... You must send a troup of Marines
to eliminate the intruders. Launch a 42school/marine-squad in two replicas,
and make sure that the service works properly (see the documentation provided
at hub.docker.com). This service will be named... marines and will be on the
overmind network.
<a href="https://github.com/Snoopgtg/docker-1/blob/master/00_how_to_docker/28" target="blank">28</a>

29. Display all the tasks of the marines service.
<a href="https://github.com/Snoopgtg/docker-1/blob/master/00_how_to_docker/29" target="blank">29</a>

30. Increase the number of copies of the marines service up to twenty, because there’s
never enough Marines to eliminate Zergs. (Remember to take a look at the tasks
and logs of the service, you’ll see, it’s fun.)
<a href="https://github.com/Snoopgtg/docker-1/blob/master/00_how_to_docker/30" target="blank">30</a>

31. Force quit and delete all the services on the local swarm, in one command.
<a href="https://github.com/Snoopgtg/docker-1/blob/master/00_how_to_docker/31" target="blank">31</a>

32. Force quit and delete all the containers (whatever their status), in one command.
<a href="https://github.com/Snoopgtg/docker-1/blob/master/00_how_to_docker/32" target="blank">32</a>

33. Delete all the container images stored on the Char virtual machine, in one command
as well.
<a href="https://github.com/Snoopgtg/docker-1/blob/master/00_how_to_docker/33" target="blank">33</a>

34. Delete the Aiur virtual machine without using rm -rf.
<a href="https://github.com/Snoopgtg/docker-1/blob/master/00_how_to_docker/34" target="blank">34</a>


## Dockerfiles

### Exercise 00: vim/emacs

  From an alpine image you’ll add to your container your favorite text editor, vim or
emacs, that will launch along with your container.
<a href="https://github.com/Snoopgtg/docker-1/blob/master/01_dockerfiles/ex00/Dockerfile" target="blank">00</a>

### Exercise 01: BYOTSS
  From a debian image you will add the appropriate sources to create a TeamSpeak
server, that will launch along with your container. It will be deemed valid if at least
one user can connect to it and engage in a normal discussion (no far-fetched setup), so
be sure to create your Dockerfile with the right options. Your program should get the
sources when it builds, they cannot be in your repository.
<a href="https://github.com/Snoopgtg/docker-1/blob/master/01_dockerfiles/ex01/Dockerfile" target="blank">01</a>

### Exercise 02: Dockerfile in a Dockerfile... in a Dockerfile ?
  You are going to create your first Dockerfile to containerize Rails applications. That’s
a special configuration: this particular Dockerfile will be generic, and called in another
Dockerfile, that will look something like this:
```
FROM ft-rails:on-build
EXPOSE 3000
CMD ["rails", "s", "-b", "0.0.0.0", "-p", "3000"]
```
Your generic container should install, via a ruby container, all the necessary dependencies
and gems, then copy your rails application in the /opt/app folder of your
container. Docker has to install the approtiate gems when it builds, but also launch
the migrations and the db population for your application. The child Dockerfile should
launch the rails server (see example below). If you don’t know what commands to use,
it’s high time to look at the Ruby on Rails documentation.
<a href="https://github.com/Snoopgtg/docker-1/blob/master/01_dockerfiles/ex02" target="blank">02</a>
