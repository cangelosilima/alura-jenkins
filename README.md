## SETUP CI
```bash
docker-compose -f ./docker/docker-compose.yml up -d
```

### GET INITIAL ADMIN PASSWORD

Find jenkins container
```bash
docker ps
```

Enter container
```bash
docker exec -i -t <container_id> /bin/bash
```

Once inside de shell, then access teh generated password
```bash
cat /var/jenkins_home/secrets/initialAdminPassword
```

