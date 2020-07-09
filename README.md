# gateone
docker_gateone安装

1.拉取docker版gateone并创建容器，将/etc/gateone/映射到本地，端口映射本地8888:
```
sudo docker run -d --name=gateone -v /etc/gateone/:/etc/gateone/ -p 8888:8000 liftoff/gateone
```
2.防火墙开放8888端口：
```
sudo firewall-cmd --zone=public --add-port=8888/tcp --permanent
sudo firewall-cmd --reload
```
