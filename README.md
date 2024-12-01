# devops-samples

This repository contains explaination of self executable file with example implemented using python. This repository also contains procedure for creating docker image.

## Folder structure

    ├── dist_python       
    │   └── executable   
    │       ├──.github
    │       │   └── workflows
    │       │       └── docker_image.yml            # This file is used for creating CI pipeline which will create an image of the self executbale file and store it in docker hub repository.
    |       ├──build
    |       │  └── main
    |       │      └── extra folder/files
    |       ├──dist
    |       │  └── main.exe                         # This is the self executable file in .exe format
    |       ├──Dockerfile                           # This is the configuration file
    |       ├──README.md                            # This file contains information about self executable file, its cloning procedure, docker image creation and running image in a container. 
    |       └──main.py                              # Source code or the main script which will carry out the function
    │
    └── README.md                                   # You are here !      
   
