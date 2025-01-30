# TG-RAG



### Run docker
```
cd GRUtopia
```

```
sudo docker run --name grutopia -it --rm --gpus all --network host \
  -e "ACCEPT_EULA=Y" \
  -e "PRIVACY_CONSENT=Y" \
  -e "WEBUI_HOST=127.0.0.1" \
  -v /home/ubuntu2404/GRUtopia:/isaac-sim/GRUtopia \
  -v $HOME/docker/isaac-sim/cache/kit:/isaac-sim/kit/cache:rw \
  -v $HOME/docker/isaac-sim/cache/ov:/root/.cache/ov:rw \
  -v $HOME/docker/isaac-sim/cache/pip:/root/.cache/pip:rw \
  -v $HOME/docker/isaac-sim/cache/glcache:/root/.cache/nvidia/GLCache:rw \
  -v $HOME/docker/isaac-sim/cache/computecache:/root/.nv/ComputeCache:rw \
  -v $HOME/docker/isaac-sim/logs:/root/.nvidia-omniverse/logs:rw \
  -v $HOME/docker/isaac-sim/data:/root/.local/share/ov/data:rw \
  -v $HOME/docker/isaac-sim/documents:/root/Documents:rw \
  grutopia:0.0.1
```

```
python GRUtopia/demo/h1_house.py
```

### Modify h1_house.yaml
To change the camera location, modify the yaml file. The cctvs are created as new robots. 

### View the environment with WebRTC
Use link: ```http://127.0.0.1:8211/streaming/webrtc-demo/?server=127.0.0.```




