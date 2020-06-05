mkdir lab3

cd lab3

gedit Dockerfile

mkdir public-html

cd public-html

gedit index.html

cd ..

docker build -t webserver .

docker run -dit --name=web -p 8080:80 webserver

docker stop $(docker ps -aq)

docker rm $(docker ps -aq)

docker rmi webserver