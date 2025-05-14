# bastard-pixel-battle-server
## Description
bastard-pixel-battle server, if you want to run your own one.

checkout client - https://github.com/frobe11/bastard-pixel-battle
## Server
### .env params
store .env with binary, at same directory.
- `PORT` - port to run server on.
### how to start server?
firstly open project directory in terminal
#### manual from sources
```bash
mkdir build
cd build
cmake ..
make
sudo ./BastardPixelBattleServer
```
#### in docker-container
```bash
docker build -t bpb-server -f DockerFile .
docker run -d -p <container_port>:8080 bpb-server &
```
#### with ansible
1. create or copy yor inventory file
2. run `ansible-playbook -i inventory.ini server-playbook.yaml`