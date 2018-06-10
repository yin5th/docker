## About
- Based on docker image nginx 

## How to use?
### Build image
1. docker build -t custom-nginx .
### Start container
2. docker run --name custom-container -d -p 80 -v your/path/sites-enabled:/etc/nginx/sites-enabled  custom-nginx


