## Docker

### Install

```
sudo pacman -S docker docker-compose
```

```
sudo usermod -a -G docker $USER
```

```
sudo systemctl enable docker
sudo systemctl start docker
```

### Aliyun mirror

```
sudo mkdir -p /etc/docker
sudo tee /etc/docker/daemon.json <<-'EOF'
{
  "registry-mirrors": ["https://xxxxxxxx.mirror.aliyuncs.com"]
}
EOF
sudo systemctl daemon-reload
sudo systemctl restart docker
```
