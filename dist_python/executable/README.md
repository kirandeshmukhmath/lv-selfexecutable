# Self executable python file

## What is python self executable file ?
The self executable file is a software which will carry out some functions after running it on any machine. The self executable file will run on any operating system.For example a self executbale file will read data from a remote excel sheet and display/store the same data in current machine. This function is carried out by the script which will run after running the file.

In the same way we have created a self executable file using python which will read data from remote excel sheet and save the same data in local machine in json file. 

## Requirements

- Python
- Any IDE (Visual Studio Code) #recommended
- Pyinstaller (python package)
- gspread 
- Service account in google developer console
- Google Suite (Excel)

## Procedure for creating self executable file

- **First create an excel sheet and add data to it (you can add some data as shown below):**

![image](https://user-images.githubusercontent.com/105641357/188873125-960d941e-64fe-4cd6-9ad7-eefc2fc20800.png)

- **Create a service account in google developer console with excel API enabled:**

*You can view this video for creating service account and downloading credentials - https://www.youtube.com/watch?v=ddf5Z0aQPzY*

![image](https://user-images.githubusercontent.com/105641357/188873389-5cf85e77-8d79-45a0-ba9b-f2139976788a.png)

- **Now lets write self executable script as shown below:**

![image](https://user-images.githubusercontent.com/105641357/188875218-fc873dc4-1e3d-4a7e-8765-5a7f9c34d43f.png)

- **Run the code by typing **python file_name.py** in the command prompt**

*The data from the remote excel sheet will be displayed in the console and also a new json file will be generated which will contain the excel sheet data.*

***Now we are able to run the self executbale file, next part is to make this file run on every machine***

*For making the file run on all possible machine we need to package all the dependencies/requirements/packages of this project into one file and create a .exe file.*

For this purpose we need to install **Pyinstaller**

- You can install **Pyinstaller** using pip (type pip install pyinstaller in command prompt)

Lets create a .exe file using Pyinstaller:

- Move to the same path where the  is file_name.py is present and type **pyinstaller --onefile pythonScriptName.py**.
- After running the above mentioned command to files naming '**build**' and '**dist**' will be created and the .exe file will be in the '**dist**' folder.
- The .exe file will be saved as file_name.exe and you just have to double click on this file and the script will run and a json file will be created in the same folder.

*Note : We know that we cannot share the .exe file to other workstations (machine), so we can solve this problem by creating an image of the .exe file*

## Creating Docker image of the self executable file

Steps Involved:

- Create an account in Dockerhub and install Docker desktop

- Open the docker desktop in your local machine and sign in and minimize it for some time and open IDE (VScode) 

- Add docker extensions in visual studio code

- Create a **dockerfile** as shown in below picture

![image](https://user-images.githubusercontent.com/105641357/188886057-1c432f1f-48bb-47cd-80ea-a7d2acf67b82.png)

- Docker can build images automatically by reading the instructions from a Dockerfile.

- A Dockerfile is a text document that contains all the commands a user could call on the command line to assemble an image.

![image](https://user-images.githubusercontent.com/105641357/188886830-ac139324-0cba-4895-bbc2-688cedcb2039.png)

- Using docker build users can create an automated build that executes several command-line instructions in succession

- Type the cmd: docker build –t imagename which will create an image which can be viewed in docker desktop application

- Type the cmd: docker run imagename which will run the image and display the output in the same console

- Once the image is created, the image will appear in docker hub and docker desktop remote repository

![image](https://user-images.githubusercontent.com/105641357/188895786-7d9f2f67-abcc-4545-a400-92afdd8ca00f.png)

### Running the image in container

- On pulling the latest image to the local repository and running it

![image](https://user-images.githubusercontent.com/105641357/188895865-50d8c0c1-4402-44b2-9dc9-f87d98536053.png)

- Image will run in the container and the required output of the python script will displayed

![image](https://user-images.githubusercontent.com/105641357/188895955-e2ae0fcc-9e93-48e3-9417-2ea37b39340f.png)
