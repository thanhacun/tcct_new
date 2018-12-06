- Docker command

    `docker run -d --rm --name container_name -v volume_name:/workspace 
    -p 8181:8181 -p 8000:8000  sapk/cloud9 --auth username:password`
    
    When running in windows somehow `yarn develop` command has errors -> has to use
    use `volume` to mount code directory

- How to copy git code into a docker volume

    `docker volume create volume_name` to create docker volume
    
    `docker run -it --rm -v ${HOME}:/root -v volume_name:/git alpine/git 
    clone git_repository .` to clone a repository into the volume.
    
    Please refer [Alpine Git](https://hub.docker.com/r/alpine/git/) for more detail.