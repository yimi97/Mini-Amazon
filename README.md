## Prerequisites
1. [UPS](https://github.com/dentiny/UPS)
2. [World Simulator](https://github.com/yunjingliu96/world_simulator_exec)


## Instruction
You should first run World server and then Amazon servers and UPS server. 


## Run Amazon Servers
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
  
