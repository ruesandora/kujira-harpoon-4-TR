<h1 align="center">Kujira harpoon-4</h1>

# Kujira harpoon-4 node kurulum rehberine hoş geldiniz

![image](https://user-images.githubusercontent.com/101149671/173236767-6cab6717-39b5-4a59-8c58-40bae1ad27da.png)

# Sistem kurulumları:
```
cd $HOME
sudo apt update
sudo apt install make clang pkg-config libssl-dev build-essential screen git jq ncdu bsdmainutils htop -y
```

# Go kurulumu:
```
cd $HOME
wget -O go1.18.1.linux-amd64.tar.gz https://golang.org/dl/go1.18.1.linux-amd64.tar.gz
rm -rf /usr/local/go && tar -C /usr/local -xzf go1.18.1.linux-amd64.tar.gz && rm go1.18.1.linux-amd64.tar.gz
echo 'export GOROOT=/usr/local/go' >> $HOME/.bash_profile
echo 'export GOPATH=$HOME/go' >> $HOME/.bash_profile
echo 'export GO111MODULE=on' >> $HOME/.bash_profile
echo 'export PATH=$PATH:/usr/local/go/bin:$HOME/go/bin' >> $HOME/.bash_profile && . $HOME/.bash_profile
go version
```

# Kujira Kurulumu
moniker-ismi degişecek (<> beraber)
```
rm -rf $HOME/kujira-core
git clone https://github.com/Team-Kujira/core $HOME/kujira-core
cd $HOME/kujira-core
make install
sleep 1
ln -s $HOME/go/bin/kujirad /usr/local/bin/kujirad
kujirad init "<moniker-ismi>" --chain-id=harpoon-4
kujirad version
```
Version 0.4.0 olması lazım

# Seed & Ayarlar:
```
#seeds="87ea1a43e7eecdd54399551b767599921e170399@52.215.221.93:26656"
wget -O $HOME/.kujira/config/genesis.json https://raw.githubusercontent.com/Team-Kujira/networks/master/testnet/harpoon-4.json
```

# Node Başlatılması: 
```
screen -S node
kujirad start
```

# CTRL + A + D screenden çıkın ve peer adresinizi alın. Ana ekran açılınca bu komutla node id alın.
```
kujirad  tendermint show-node-id
```

# Peer Adresiniz = nodeid@ip:port - Şu Şekilde oalcaktır: 
```
" 8a11c650e5233ae6a88c825a1ee6f8c46ff81a77@148.251.64.113:26656 "
```

# DAHA FAZLA SORUNUZ VARSA KUJİRA TÜRKİYE TELEGRAM GRUBU:

[Telegram](https://t.me/KujiraTurkish)

Teşekkürler <3


# Hesaplar:

[<img src="https://cdn-icons-png.flaticon.com/512/733/733579.png" width="16px"> Twitter   ](https://twitter.com/Ruesandora0) 
[<img src="https://cdn-icons-png.flaticon.com/512/1336/1336494.png" width="16px"> Forum   ](https://forum.rues.info/index.php)
[<img src="https://cdn-icons-png.flaticon.com/512/2111/2111646.png" width="16px"> Telegram Announcement   ](https://t.me/RuesAnnouncement)
[<img src="https://cdn-icons-png.flaticon.com/512/2111/2111646.png" width="16px"> Telegram Chat   ](https://t.me/RuesChat)
[<img src="https://cdn-icons-png.flaticon.com/512/2111/2111646.png" width="16px"> Telegram Node   ](https://t.me/RuesNode)
[<img src="https://cdn-icons-png.flaticon.com/512/2111/2111646.png" width="16px"> Telegram Node Chat](https://t.me/RuesNodeChat)
