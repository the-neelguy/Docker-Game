# Docker-Game

Containerized an existing game called 2048 using Docker and deployed the same in Elastic Beanstalk of AWS

STEPS TO FOLLOW

1. Clone the Dockerfile into a specific folder in your computer
2. Start Docker and make sure you have all the dependencies pre-installed.
3. Move on to the code editor (for eg. VS CODE) and open the terminal to write the following commands -
     a. docker build -t 2048-game .
         This command creates a docker image and downloads all the dependencies like nginx, zip and curl while executing.
     b. docker images
         This command helps you to see the docker images created in your system. If the previous step is completed successfully, you will see an image called 2048-game
     c. docker images | grep 2048
         This command will let you see the image specifications along with the image id.
     d. docker run -d -p 80:80 <image_id>
         Paste the image id in the command and this will run and create a container out of the docker image.

4. Once it is done, to verify, you can move to your browser and type http://localhost:80 and the 2048 game should appear.
5. Next move to the AWS Console and under services click on Compute. Select Elastic Beanstalk from the options.
6. Make sure you have an EC2 Instance created with a proper secret key pair.
7. Now follow the on screen instructions for the Beanstalk app creation.
8. Under platform choose - Docker and upload your source code i.e. the dockerfile and provide it a version name.
9. Make sure to choose a free-tier orelse you will be charged based upon your usage.
10. Once it is done, click on deploy and it will take some time to deploy this application
11. Once done, you can click on the link (like http://2048game-env.eba-u3tfyvwv.ap-south-1.elasticbeanstalk.com/ ) and you will be redirected to the game page.
12. Make sure to stop/terminate the application once done, as it make exceed the benefits of free-tier if you keep it running.

# SCREENSHOTS

![image](https://github.com/the-neelguy/Docker-Game/assets/77458394/7413c4b9-aa3e-4593-a8fc-b31683ac6f93)

![image](https://github.com/the-neelguy/Docker-Game/assets/77458394/24b9d0b6-65e2-4e03-8dff-f29610a96718)

![image](https://github.com/the-neelguy/Docker-Game/assets/77458394/c608982d-3e77-46ce-a459-84c6427659a6)


