# WOW - Trinity Core - Docker


> 地址都用了镜像. 理论上无需梯子.



## Build

```bash
docker build -t wow -f TrinityCore-3.3.5/Dockerfile TrinityCore-3.3.5;
```



## Run

```bash
docker run --rm -it \
	-v /wow/app:/appdata \
	--name wow \
	-p 8085:8085 -p 3724:3724 -p 3306:3306 \
	-e EXTERNAL_ADDRESS=127.0.0.1 \
    -v /wow/TrinityCore-3.3.5/entrypoint.sh:/entrypoint.sh \
	wow:335;
```
