# Experiment 2: Docker Volume

## Aim
To use and understand Docker Volume. Create a shared volume between 2 containers to share files.

## Steps Performed
 - Run two containers with single attached volume `docker run -it -v mVol:/mnt ubuntu`
![image2](https://user-images.githubusercontent.com/46739435/107741455-34b57900-6d33-11eb-9724-af374b6b9d4d.png)

 - Run `docker ps` to list running containers.
![image4](https://user-images.githubusercontent.com/46739435/107741458-35e6a600-6d33-11eb-8491-1dca7b88fb14.png)

- Create a file in Docker A. `touch a.txt`
![image3](https://user-images.githubusercontent.com/46739435/107741457-354e0f80-6d33-11eb-8943-9c443eaf1e95.png)

- File a.txt can also be listed in Docker B (shared volume). `ls`
![image1](https://user-images.githubusercontent.com/46739435/107740587-7e9d5f80-6d31-11eb-8a81-1867a777df58.png)

- Inspect docker volume using `docker volume inspect mVol`
![image5](https://user-images.githubusercontent.com/46739435/107741459-367f3c80-6d33-11eb-8b5f-293a78899a90.png)