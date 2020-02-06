# deepin-env-setup

#### 先下載 deepin 的 ISO 檔

http://ftp.tku.edu.tw/Linux/Deepin/deepin-cd/15.11/

#### 把 ISO 檔 dd 到 SD 卡上面

    dd if=deepin-15.11-amd64.iso of=/dev/rdisk1 bs=10m

#### 裝到 Supermicro 的 SSD 
#### 安裝 AnyDesk

    echo mynewpassword | sudo anydesk --set-password
    
- Cannot access security panel from anydesk https://askubuntu.com/a/1147612/561540    

#### 安裝 Room
#### 安裝 ssh

- Enable SSH Server on Debian https://linuxhint.com/enable-ssh-server-debian/

      sudo apt-get install openssh-server

#### 安裝 Nodejs

    $ cd ~
    $ cd Downloads
    $ sudo apt-get install curl
    
###### 目前最新 LTS 版本為 12.x 版

    $ curl -sL https://deb.nodesource.com/setup_12.x | sudo -E bash -
    $ sudo apt-get install nodejs
    $ node -v
    v12.14.1
    $ npm -v
    6.13.4
      
###### How to Install Latest Node.js and NPM on Ubuntu with PPA<br>
###### https://tecadmin.net/install-latest-nodejs-npm-on-ubuntu/

#### 安裝 Vue

    cnmp install vue
    sudo cnpm install --global vue-cli
    
#### 建立第一個 Vue 的 project

    $ vue init webpack my-project
    $ cd my-project
    $ npm run dev
    Your application is running here: http://localhost:8080
    
#### 設定 host 
    
- 修改 config/index.js

      //host: 'localhost', // can be overwritten by process.env.HOST
      host: '0.0.0.0', // can be overwritten by process.env.HOST
      
- 設定環境變數

      $ export HOST=0.0.0.0
      $ npm run dev
      Your application is running here: http://0.0.0.0:8080
      
      $ sudo netstat -tulpn
      
 ![](https://github.com/Charles-Hsu/deepin-env-setup/blob/master/netstat-tulpn.png)
 
 ![](https://github.com/Charles-Hsu/deepin-env-setup/blob/master/vue.png)
    
   
