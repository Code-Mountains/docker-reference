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

## View Azure ACR Repo List:
```
$ az acr repository list --name testacrr.azurecr.io --output table
The login server endpoint suffix '.azurecr.io' is automatically omitted.
Result
---------------------
hello-world-nginx-app
```

## Show tags for a repo in ACR:
```
$ az acr repository show-tags --name testacrr --repository hello-world-nginx-app
[
  "latest"
]
```
