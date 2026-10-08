```text
PS C:\Users\ACER\Documents\DevOps\SS9\ex3> docker images
                                                                                                     i Info →   U  In Use
IMAGE                          ID             DISK USAGE   CONTENT SIZE   EXTRA
apache/kafka:4.0.1             9a129e03121d        620MB          221MB    U   
confluentinc/cp-kafka:latest   0ad069035863        876MB          304MB    U   
hello-world:latest             5e2309035332       25.9kB         9.49kB    U   
my-html-app:v1                 8b5a555b404f       93.6MB         26.3MB        
redis:latest                   298e5b3bc566        212MB         57.5MB    U   
PS C:\Users\ACER\Documents\DevOps\SS9\ex3> docker run -d -p 8081:80 --name html-app my-html-app:v1
8948784f2bf2bf76e436d388e1042f2eb8e61de7330a25de75542b816d124584
PS C:\Users\ACER\Documents\DevOps\SS9\ex3> docker ps                                              
CONTAINER ID   IMAGE            COMMAND                  CREATED          STATUS          PORTS                                     NAMES
8948784f2bf2   my-html-app:v1   "/docker-entrypoint.…"   13 seconds ago   Up 13 seconds   0.0.0.0:8081->80/tcp, [::]:8081->80/tcp   html-app
PS C:\Users\ACER\Documents\DevOps\SS9\ex3> curl.exe http://localhost:8081
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
<body>
    <h1>Hello Docker Session 09!</h1>
</body>
</html>
```