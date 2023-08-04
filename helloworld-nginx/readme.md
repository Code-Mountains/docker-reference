## Build Docker Image:
```
$ docker build -t hello-world-nginx-app .
[+] Building 5.7s (10/10) FINISHED                                                                                                                                                                             
 => [internal] load .dockerignore                                                                                                                                                                         0.0s
 => => transferring context: 2B                                                                                                                                                                           0.0s
 => [internal] load build definition from Dockerfile                                                                                                                                                      0.0s
 => => transferring dockerfile: 519B                                                                                                                                                                      0.0s
 => [internal] load metadata for docker.io/library/nginx:alpine                                                                                                                                           1.3s
 => [1/5] FROM docker.io/library/nginx:alpine@sha256:2d194184b067db3598771b4cf326cfe6ad5051937ba1132b8b7d4b0184e0d0a6                                                                                     3.1s
 => => resolve docker.io/library/nginx:alpine@sha256:2d194184b067db3598771b4cf326cfe6ad5051937ba1132b8b7d4b0184e0d0a6                                                                                     0.0s
 => => sha256:6a107772494d184e0fddf5d99c877e2fa8d07d1d47b714c17b7d20eba1da01c6 626B / 626B                                                                                                                0.2s
 => => sha256:4db1b89c0bd13344176ddce2d093b9da2ae58336823ffed2009a7ea4b62d2a95 3.37MB / 3.37MB                                                                                                            0.6s
 => => sha256:2d4efe74ef541248b0a70838c557de04509d1115dec6bfc21ad0d66e41574a8a 1.99kB / 1.99kB                                                                                                            0.0s
 => => sha256:4937520ae206c8969734d9a659fc1e6594d9b22b9340bf0796defbea0c92dd02 16.69kB / 16.69kB                                                                                                          0.0s
 => => sha256:bd338968799fef766509223449d72392692f1f56802da9059ae3f0965c2885e2 1.93MB / 1.93MB                                                                                                            0.7s
 => => sha256:2d194184b067db3598771b4cf326cfe6ad5051937ba1132b8b7d4b0184e0d0a6 1.65kB / 1.65kB                                                                                                            0.0s
 => => sha256:9f05b0cc5f6e8010689a6331bad9ca02c62caa226b7501a64d50dcca0847dcdb 957B / 957B                                                                                                                0.3s
 => => sha256:4c5efdb87c4a2350cc1c2781a80a4d3e895447007d9d8eac1e743bf80dd75c84 366B / 366B                                                                                                                0.5s
 => => sha256:c8794a7158bff7f518985e76c590029ccc6b4c0f6e66e82952c3476c095225c9 1.21kB / 1.21kB                                                                                                            0.7s
 => => extracting sha256:4db1b89c0bd13344176ddce2d093b9da2ae58336823ffed2009a7ea4b62d2a95                                                                                                                 0.4s
 => => sha256:768e67c521a97f2acf0382a9750c4d024fc1e541e22bab2dec1aad36703278f1 11.65MB / 11.65MB                                                                                                          1.8s
 => => sha256:8de2a93581dcb1cc62dd7b6e1620bc8095befe0acb9161d5f053a9719e145678 1.40kB / 1.40kB                                                                                                            0.8s
 => => extracting sha256:bd338968799fef766509223449d72392692f1f56802da9059ae3f0965c2885e2                                                                                                                 0.6s
 => => extracting sha256:6a107772494d184e0fddf5d99c877e2fa8d07d1d47b714c17b7d20eba1da01c6                                                                                                                 0.0s
 => => extracting sha256:9f05b0cc5f6e8010689a6331bad9ca02c62caa226b7501a64d50dcca0847dcdb                                                                                                                 0.0s
 => => extracting sha256:4c5efdb87c4a2350cc1c2781a80a4d3e895447007d9d8eac1e743bf80dd75c84                                                                                                                 0.0s
 => => extracting sha256:c8794a7158bff7f518985e76c590029ccc6b4c0f6e66e82952c3476c095225c9                                                                                                                 0.0s
 => => extracting sha256:8de2a93581dcb1cc62dd7b6e1620bc8095befe0acb9161d5f053a9719e145678                                                                                                                 0.0s
 => => extracting sha256:768e67c521a97f2acf0382a9750c4d024fc1e541e22bab2dec1aad36703278f1                                                                                                                 0.9s
 => [internal] load build context                                                                                                                                                                         0.0s
 => => transferring context: 494B                                                                                                                                                                         0.0s
 => [2/5] RUN rm /etc/nginx/conf.d/default.conf                                                                                                                                                           0.6s
 => [3/5] COPY nginx.conf /etc/nginx/conf.d/                                                                                                                                                              0.0s
 => [4/5] RUN mkdir -p /usr/share/nginx/html/app                                                                                                                                                          0.5s
 => [5/5] COPY index.html /usr/share/nginx/html/app                                                                                                                                                       0.1s
 => exporting to image                                                                                                                                                                                    0.1s
 => => exporting layers                                                                                                                                                                                   0.1s
 => => writing image sha256:3ceb749a9a1fba5f7e4336282bdf30cc4ac6b208cc45a34404a9070dfcaf4bdb                                                                                                              0.0s
 => => naming to docker.io/library/hello-world-nginx-app             
```

## You should see this new image locally now:
```
$ docker images
REPOSITORY                       TAG           IMAGE ID       CREATED          SIZE
hello-world-nginx-app            latest        3ceb749a9a1f   51 seconds ago   41.4MB
```

## Tag this image before pushing it off to Azure ACR:
```
$ docker tag hello-world-nginx-app testacrr.azurecr.io/hello-world-nginx-app:latest
```

## You should be able to see another tagged imaged show up with acr in the name:
```
$ docker images
REPOSITORY                                  TAG           IMAGE ID       CREATED         SIZE
hello-world-nginx-app                       latest        3ceb749a9a1f   2 minutes ago   41.4MB
testacrr.azurecr.io/hello-world-nginx-app   latest        3ceb749a9a1f   2 minutes ago   41.4MB
```

## Then push image to Azure ACR:
```
$ docker push testacrr.azurecr.io/hello-world-nginx-app:latest
The push refers to repository [testacrr.azurecr.io/hello-world-nginx-app]
5f5aca18dd8c: Pushed 
42cf935afe9e: Pushed 
bfc6952c0302: Pushed 
2f01dad06f4a: Pushed 
bdea7c663e86: Pushed 
1b22827e15b4: Pushed 
d9f50eaf56fa: Pushed 
2530717ff0bb: Pushed 
e7766bc830a8: Pushed 
cb411529b86f: Pushed 
bc09720137db: Pushed 
3dab9f8bf2d2: Pushed 
latest: digest: sha256:6a83dc5bb96abe0b4f366323a60305e853d97159814cb9d6dbce9757729a6e58 size: 2817
```

## Login to your Azure Container Registry (ACR)
```
$ docker login testacrr.azurecr.io --username testacrr
Password: 
WARNING! Your password will be stored unencrypted in /home/sysadmin/.docker/config.json.
Configure a credential helper to remove this warning. See
https://docs.docker.com/engine/reference/commandline/login/#credentials-store

Login Succeeded
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
