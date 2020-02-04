# deepin-env-setup

###### 先下載 deepin 的 ISO 檔

http://ftp.tku.edu.tw/Linux/Deepin/deepin-cd/15.11/

###### 把 ISO 檔 dd 到 SD 卡上面

    dd if=deepin-15.11-amd64.iso of=/dev/rdisk1 bs=10m

###### 裝到 Supermicro 的 SSD 
###### 安裝 AnyDesk

    echo mynewpassword | sudo anydesk --set-password
    
- Cannot access security panel from anydesk https://askubuntu.com/a/1147612/561540    

###### 安裝 Room
###### 安裝 ssh

- Enable SSH Server on Debian https://linuxhint.com/enable-ssh-server-debian/

      sudo apt-get install openssh-server

###### 安裝 Nodejs

    cd /usr/local/lib
    sudo mkdir nodejs
    cd nodejs
    wgets https://nodejs.org/dist/v12.14.1/node-v12.14.1-linux-x64.tar.xz
    tar xf node-v12.14.1-linux-x64.tar.xz
    cd /etc/profile.d
    sudo touch nodejs-env.sh
    sudo vi nodejs-env.sh
    export NODEJS_HOME=/usr/local/lib/nodejs/node-v8.9.4
    export PATH=$NODEJS_HOME/bin:$PATH
    
- 因為是手動安裝的, 需要設定路徑

      sudo ln -s /usr/local/lib/nodejs/node-v12.14.1-linux-x64/bin/node /usr/bin/node
      
