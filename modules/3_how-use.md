Build vs. Buy (re-use)


1. Existing ananlysis / workflows are out there
    WDL, docker and config (possibly even public data)
2. Tools/scripts have been 'dockerized' for Bioinformatics

Docker Terms
    --Docker Image - runnable version of Docker container
        *images can be located in several locations
            -- on you local machine
            -- on a public registry (DockerHub, GCR-public...)
            -- on a private registry (GCR-private...)
    --Dockerfile - definition of Docker container
    --Building -> creating a runnable docker image (or container) from a Dockerfile
        *docker build....
    --Running -> running a container image using the Docker daemon
        *can run locally, can run in cloud, etc...
        *docker pull .... (checks to see if you have the image locally, if not it 'pulls'
            the image using layers)
    --Monitoring -> viewing running docker containers on an environment
        * docker ps...

 3. Easier to re-use existing containers than create new ones
        find -> pull -> run -> verify (you can run on cloud VM to test)

        How do I find a good quality container?
            How large is it?
            Does the tool/script work?
            What is the config?
            What tools are included?
            Is the init working?
            Who made it / where is it used?

  4. Building requires installation and configuration of locally installed tools
        configure tools (Docker), create Dockerfile (using best practices), 
            test Docker container locally
            deploy built image to Docker registry (DockerHub, etc...)
        integrate container into analysis/workflow
            find or create WDL
            test workflow (locally?)
            deploy to execution environment (Terra, FC, other...)
        

