# Troubleshooting-Found-Orphan-Container-
![image](https://user-images.githubusercontent.com/99332618/234415417-2be81292-47a0-4ab9-b611-37dc2e6b75c6.png)

What the above error does is that it blocks the other containers from running. This happens most times for docker compose files.

SOLUTION:

1. Make sure to have different networks declared in the docker-compose file of each container. e.g.

![image](https://user-images.githubusercontent.com/99332618/234416887-34efa1cc-6625-4a47-b7b2-1085bcf4381c.png)


2. Use different names to run docker-compose files:

docker-compose -f docker-compose.yml --project-name my-project up -d

OR 

docker-compose -f docker-compose.yml -p my-project up -d

![image](https://user-images.githubusercontent.com/99332618/234416480-8ed3ee8e-cdc6-49bd-9b28-53f68579f80a.png)
