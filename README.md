# Welcome to dockermgr youtubedlmaterial installer 👋
  
## Web frontend for youtube-dl  
  
### Requires scripts to be installed

```shell
 sudo bash -c "$(curl -LSs <https://github.com/dockermgr/installer/raw/main/install.sh>)"
 dockermgr --config && dockermgr install scripts  
```

#### Automatic install/update  

```shell
dockermgr install youtubedlmaterial
```


#### Manual install

```shell
git clone https://github.com/dockermgr/youtubedlmaterial "$HOME/.local/share/CasjaysDev/dockermgr/youtubedlmaterial"
bash -c "$HOME/.local/share/CasjaysDev/dockermgr/youtubedlmaterial/install.sh"
```
  
#### Just run it

```shell
mkdir -p "$HOME/.local/share/srv/docker/youtubedlmaterial/"

git clone <https://github.com/dockermgr/youtubedlmaterial> "$HOME/.local/share/CasjaysDev/dockermgr/youtubedlmaterial"

cp -Rfva "$HOME/.local/share/srv/docker/youtubedlmaterial/dataDir/." "$HOME/.local/share/srv/docker/youtubedlmaterial/"

sudo docker run -d \
--name="youtubedlmaterial" \
--hostname "youtubedlmaterial" \
--restart=always \
--privileged \
-e TZ="${TZ:-${TIMEZONE:-America/New_York}}" \
-v "$HOME/.local/share/srv/docker/youtubedlmaterial/files/data":/data:z \
-v "$HOME/.local/share/srv/docker/youtubedlmaterial/files/config":/config:z \
-p PORT:INT_PORT \
TEMPLATE/TEMPLATE 1>/dev/null
```

## Author  

👤 **Jason Hempstead**  
