## Prerequisites
```
cd Mini-Amazon/server-docker/server
pip3 install protobuf
sudo apt install protobuf-compiler
protoc -I=. --python_out=. ./world_amazon.proto
protoc -I=. --python_out=. ./UA.proto
```

## Run
1. Frontend Server
- Modify `/frontend-docker/web-app/frontEndServer/views.py` `AMAZON_HOST` to your hostname
- Run Frontend Server with 
    ```
    cd Mini-Amazon/frontend-docker/
    sudo docker-compose up
    ```
2. Amazon Server
- Modify `/server-docker/server/run_server.py` `WORLD_HOST` to world hostname
- `UPS_PORT` (default `5555`)
- Run Amazon Server with 
    ```
    cd Mini-Amazon/server-docker/
    sudo docker-compose up
    ```
