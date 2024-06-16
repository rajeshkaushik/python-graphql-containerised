# python-graphql-containerised
# It's a Python GraphQL API project leveraging Podman for containerizing the API

# Podman commands cheatsheet

podman machine start    # start the vm on local

podman info

podman machine ssh  # ssh to vm

podman login docker.io  # login to dockerhub

podman search graphene  # search repository

Podman images   # list images

podman build -t django-graphql-app-rajesh . -f Podfile  # create image

podman run -p 8000:8000 django-app  # run django app in container

podman ps   # show running containers

podman push django-graphql-app-rajesh docker.io/rajeshkaushik15/django-graphql-app-rajesh   # push image to docker, login is required

podman machine stop

podman rmi $(podman images -qa) -f  # remove all images from local for cleanup. ***Be carefull***
