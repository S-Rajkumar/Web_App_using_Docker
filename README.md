#Web_APP_using_Docker
>list docker images [local]
`docker image ls`

#delete docker image from local
>docker image rm -f <image_id>

`docker image rm -f 4dcb4cd166ee`

#build image using Dockerfile
>docker build -t <tag_name> <Dockerfile_location>

`docker build -t webapp .`

#run a docker image
>docker run -p <Expose_Post>:<Docker_Expose_port>  <image_id or tag_name>

`docker run -p 80:80 6f6fd3d7d9bf`

#run a docker image with volume ( no need to create image after changes in the directory/file )
>docker run -p 80:80 -v /src/:/dest/ <image_id or tag_name> [path must be an absolute path]

`docker run -p 80:80 -v /home/smiley/Documents/Docker/Web_App_using_Docker/WebApp/:/var/www/html webapp`
