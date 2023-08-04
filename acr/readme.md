## Login to your Azure Container Registry (ACR)
```sysadmin@ub22:~$ docker login testacrr.azurecr.io --username testacrr
Password: 
WARNING! Your password will be stored unencrypted in /home/sysadmin/.docker/config.json.
Configure a credential helper to remove this warning. See
https://docs.docker.com/engine/reference/commandline/login/#credentials-store

Login Succeeded
```

## List Locally available images:
```
sysadmin@ub22:~$ docker images
REPOSITORY                       TAG           IMAGE ID       CREATED        SIZE
mcr.microsoft.com/mssql/server   2019-latest   330e92fa0cc2   2 months ago   1.47GB
```

## Tag this local image before pushing it off to ACR:
docker 
