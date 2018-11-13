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

