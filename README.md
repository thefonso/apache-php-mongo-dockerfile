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
 docker run <name-of-image>
 ```
 GET Container_ID from running image process
 
 ```
 docker ps
 ```
 
 GET PROMPT:
 ```
 docker exec -i -t <container_ID> /bin/bash
 ```

### Contents

- MONGO V2.2.7
- PGP 2.2
- PHP 1.5.5
- Apache V2

