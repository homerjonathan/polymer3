docker run -it -v $(pwd):/root/app elswork/polymer3 yarn init
docker run -it -v $(pwd):/root/app elswork/polymer3 yarn install
docker run -d -p 8081:8081 --name poly3test -v $(pwd):/root/app elswork/polymer3 polymer serve --port 8081 -H 0.0.0.0 --npm