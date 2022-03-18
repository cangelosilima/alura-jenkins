# JENKINS AND .NET CORE TUTORIAL

## SETUP APP AND CI
To run docker
```bash
docker-compose -f ./docker/docker-compose.yml up -d
```

## APP

### RUN STANDALONE
Run .net core
```bash
dotnet run --project  ./src/application/application.csproj
```

At your web browser access http://localhost:8080

## SETUP CI
To run jenkins (if now already up)
```bash
docker-compose -f ./docker/docker-compose.yml up -d
```

### JENKIS
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

### ACCESS JENKINS
At your web browser access http://localhost:8080