## Update to Nillion verifier v1.0.1 docker image
### 1. Stop and remove your docker
```Bash
docker ps | grep nillion | awk '{print $1}' | xargs docker stop
```
```Bash
docker ps -a | grep nillion | awk '{print $1}' | xargs docker rm
```
### 2. Run docker with new version
```Bash
sudo docker run -d -v ./nillion/accuser:/var/tmp nillion/verifier:v1.0.1 verify --rpc-endpoint "https://testnet-nillion-rpc.lavenderfive.com"
```
### 3. Check docker log
```Bash
docker ps -a | grep nillion | awk '{print $1}' | xargs docker logs -f
```
