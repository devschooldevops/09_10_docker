## Quiz
### Question 1:
#### If you wanted to view running containers as well as containers that you have stopped and not removed, what command would you use?
- [ ] docker container ls
- [ ] docker container ps
- [ ] docker container ls -a
- [ ] docker list containers

### Question 2:
#### What does the -d flag do in a docker run command?
- [ ] It detaches the container to run in the background, and returns you to the shell prompt
- [ ] -d publishes a port of our choosing
- [ ] -d means detach, so the container runs on a different server we specify at runtime
- [ ] -d means delete the container when we are done with it

### Question 3:
#### Would the following two commands create a port conflict error with each other?
`docker container run -p 80:80 -d nginx`\
`docker container run -p 8080:80 -d nginx`
- [ ] Yes
- [ ] No

<i>Hint: the docker port publishing format of < public port >:< container port >.

Port conflict errors occur when multiple services are running on the same published port on the same host</i>

### Question 4:
#### I ran 'docker container run -p 80:80 nginx' and my command line is gone and everything looks frozen. Why?
- [ ] Because the port you are trying to run the command on is in use by another container
- [ ] Because you have too many nginx containers running and your system is out of memory
- [ ] Because you didn't specify the -d flag to detach it in the background, and there aren't any Nginx logs yet
- [ ] Because nginx is tired of giving you access to open source images for free without any donations and you need to give them money before using the image again

🌌 **[Let's continue](class-2.md)**