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
    
- 因為是手動安裝的, 需要設定路徑 (解決 npm 執行後跑出 node not found 的問題)

      sudo ln -s /usr/local/lib/nodejs/node-v12.14.1-linux-x64/bin/node /usr/bin/node
      
###### 安裝 cnpm

    $ sudo npm install -g cnpm --registry=https://registry.npm.taobao.org
    $ whereis cnpm
    cnpm: /usr/local/lib/nodejs/node-v12.14.1-linux-x64/bin/cnpm
    $ sudo ln -s /usr/local/lib/nodejs/node-v12.14.1-linux-x64/bin/cnpm /usr/bin/cnpm
    $ cnpm -v
    cnpm@6.1.1 (/usr/local/lib/nodejs/node-v12.14.1-linux-x64/lib/node_modules/cnpm/lib/parse_argv.js)
    npm@6.13.7 (/usr/local/lib/nodejs/node-v12.14.1-linux-x64/lib/node_modules/cnpm/node_modules/npm/lib/npm.js)
    node@12.14.1 (/usr/local/lib/nodejs/node-v12.14.1-linux-x64/bin/node)
    npminstall@3.27.0 (/usr/local/lib/nodejs/node-v12.14.1-linux-x64/lib/node_modules/cnpm/node_modules/npminstall/lib/index.js)
    prefix=/usr/local/lib/nodejs/node-v12.14.1-linux-x64
    linux x64 4.15.0-30deepin-generic
    registry=https://r.npm.taobao.org
    
###### 安裝 Vue

    cnmp install vue
    sudo cnpm install --global vue-cli
    
###### 建立第一個 Vue 的 project

    $ vue init webpack my-project
    $ cd my-project
    $ npm run dev
    Your application is running here: http://localhost:8080
    
###### 設定 host 
    
- 修改 config/index.js

      //host: 'localhost', // can be overwritten by process.env.HOST
      host: '0.0.0.0', // can be overwritten by process.env.HOST
      
- 設定環境變數

      $ export host=0.0.0.0
      $ npm run dev
      Your application is running here: http://0.0.0.0:8080
      
      $ sudo netstat -tulpn
      
 ![](https://github.com/Charles-Hsu/deepin-env-setup/blob/master/netstat-tulpn.png)
    
   
