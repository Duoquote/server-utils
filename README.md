# server-utils

This repo includes docker containers which I use.

## Aria2-RPC
To run aria2-rpc server you need to copy `.env.example` rename it to `.env`, change the secret value to whatever you want. Then by running `docker-compose up -d` it will start aria2-rpc on port `6890`. You can change the port in `docker-compose.yml`. You can also run this container on windows by running `docker-compose -f docker-compose.yml -f windows-compose.yml up -d`.