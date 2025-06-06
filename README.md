# Docker
### Quiz
    1. Which of the following answers is true about buildtime statements in Docker?
        a) They only effect how containers run
        b) They only effect files in the image or how the image is built
        c) They are always stored as meta data
        ans: B Correct. You could argue that how an image is built, is to affect how it will run, but you get the point here: Buildtime statements will do things during a docker build.
    2. Which of the following is true about overwrite statements?
        a) They add to any previous use.
        b) they only effect run time behaviour
        c) They replace any previous use
        ans: C
    3. Which type of statement is ENTRYPOINT?
        a) Buildtime
        b) Runtime
        c) Compile-time
        d) sleep time
        ans: B True. Docker adds the ENTRYPOINT to the metadata that goes along with the image, for it to be used on container start.
    4. How many ENTRYPOINT instructions in a Dockerfile are used?
        a) The first one
        b) All of them
        c) The last one
        ans: C True. Because ENTRYPOINT is an Overwrite statement. Only the last one in the Dockerfile is used.
    5. Which statement is preferred for starting long-lasting processes like web servers or databases?
        a) Entrypoint
        b) CMD
        c) RUN
        ans: B Default to using CMD for long running processes.
    6. When would you need to add a SHELL statement to a Dockerfile?
        a) when i want to install a new shell in the image
        b) when i want to change default shell on Linux for run statements
        c) when i want to switch from linux containers to windows containers
        d) when i want to change to distroless image
        option c: False. To create a Docker image that supports the Windows kernel, also called a “Windows Container”, you’d need to change the FROM statement to a Microsoft Windows base image.
        option B:  In the rare case you need to change from “sh” on Linux or “cmd” on Windows, SHELL is how you do it for affecting RUN, and sometimes CMD statements.
### 
