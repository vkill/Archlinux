## Docker

### Install

```
sudo pacman -S docker docker-compose docker-buildx
```

```
sudo usermod -a -G docker $USER
```

```
sudo systemctl enable docker
sudo systemctl start docker
```

### With proxy

Ref https://stackoverflow.com/questions/59246519/how-can-i-make-docker-compose-pull-images-using-a-socks5-proxy

```
sudo mkdir /etc/systemd/system/docker.service.d

sudo vim /etc/systemd/system/docker.service.d/http-proxy.conf
[Service]
Environment="HTTP_PROXY=socks5://127.0.0.1:1080"

sudo systemctl daemon-reload

sudo systemctl restart docker.socket
sudo systemctl restart docker.service
```

### With mirror

```
sudo mkdir -p /etc/docker
sudo tee /etc/docker/daemon.json <<-'EOF'
{
  "registry-mirrors": ["https://xxxxxxxx.mirror.aliyuncs.com"]
}
EOF

sudo systemctl daemon-reload

sudo systemctl restart docker.socket
sudo systemctl restart docker.service
```
