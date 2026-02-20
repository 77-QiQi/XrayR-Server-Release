# XrayR-Server-Release

## 安装 Docker & Compose 便携版

```
curl -fsSL https://get.docker.com -o get-docker.sh
sh get-docker.sh && rm -f get-docker.sh
curl -SL https://github.com/docker/compose/releases/latest/download/docker-compose-linux-x86_64 -o /usr/local/bin/docker-compose
chmod +x /usr/local/bin/docker-compose
docker-compose -v
```

## 安装 XrayR-Server

```
git clone https://github.com/77-QiQi/XrayR-Server-Release.git
cd XrayR-Server-Release/
cp config/config.yml.example config/config.yml
```
编辑 config/config.yml 文件

### 下载 geoip.dat geosite.dat
```
wget -O config/geosite.dat https://github.com/v2fly/domain-list-community/releases/latest/download/dlc.dat
wget -O config/geoip.dat https://github.com/v2fly/geoip/releases/latest/download/geoip.dat
```

### 启动 / 更新 XrayR-Server
```
docker-compose pull
docker-compose up -d
```
