## apache2 php mongo dockerfile

pull this code down to your local machine then...	

 BUILD IMAGE:
 At cli run the following.
 ```
 docker build -t <your_name> .
 ```
 (period is important. reads Dockerfile)
 
 RUN IMAGE: 
 
 ```
 docker run -tid <name-of-image> /bin/bash
 ```
 GET Container_ID from running image process
 
 ```
 docker ps
 ```
 
 GET PROMPT:
 ```
 docker exec -i -t <container_ID> /bin/bash
 ```
 ---
 
 ## run your local app
 
 navigate to app directory with it's **Dockerfile** assuming you built your local image with the name "mongo-php-apache2"...
 
 ```
 FROM mongo-php-apache2:latest
 ADD MyVhost.conf /etc/apache2/sites-enabled/
 CMD ["/run.sh"]
 ```
 
 ## run second image attached to local app
 
```
docker build -t <your-name-for-new-image> .
### (reads Dockerfile file)
### assuming image name is 750words-fonso...(run images with app code connection)

docker run -d -v /Users/aleph/Sites/750words:/var/www/html/ -p 80 750words-fonso

docker ps
### (note container_id from process names)

docker exec -i -t <container_ID> /bin/bash
```

### Contents

- MONGO V2.2.7
- PGP 2.2
- PHP 1.5.5
- Apache V2

