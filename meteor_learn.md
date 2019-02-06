### Meteor配置80端口

> 经过若干次尝试，发现root是无法启动meteor app的。。。只好放弃另寻他路。

果然搜索引擎不负众望，开启了新思路：
```
sudo iptables -t nat -A PREROUTING -p tcp --dport 80 -j REDIRECT --to-ports 300
```

搞定收工！
