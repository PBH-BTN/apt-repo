# APT-Repo

PBH-BTN Debian APT 软件源。

## 使用方式

```
Types: deb
URIs: https://apt-repo.pbh-btn.com/debian
Suites: sid
Components: main
Signed-By: /etc/apt/keyrings/pbh-btn.asc
```

将上面的内容保存到 `/etc/apt/sources.list.d/pbh-btn.sources`

并执行下面的命令

```
sudo apt update
sudo apt install ca-certificates cur -y
sudo install -m 0755 -d /etc/apt/keyrings
sudo curl -fsSL https://raw.githubusercontent.com/PBH-BTN/apt-repo/master/public-key.asc -o /etc/apt/keyrings/pbh-btn.asc
sudo chmod a+r /etc/apt/keyrings/pbh-btn.asc
sudo apt update
sudo apt search PeerBanHelper
```

即可。
