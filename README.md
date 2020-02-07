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
      
###### How to Install Latest Node.js and NPM on Ubuntu with PPA
https://tecadmin.net/install-latest-nodejs-npm-on-ubuntu/

#### 安裝 Vue

    $ sudo npm install -g @vue/cli @vue/cli-service-global
    
#### 建立第一個 Vue 的 project

    $ mkdir vue 
    $ cd vue
    $ vue create hello-world
    $ cd hello-world
    $ npm run dev
    
      App running at:
      - Local:   http://localhost:8080/
      - Network: http://192.168.1.123:8080/
      
 ![](https://github.com/Charles-Hsu/deepin-env-setup/blob/master/netstat-tulpn.png)
 
 ![](https://github.com/Charles-Hsu/deepin-env-setup/blob/master/vue.png)
 
 ##### 設定 https 為 facebook 做準備
 
    $ vi vue.config.js
    const fs = require('fs')
    module.exports = {
	  devServer: {
		      open: process.platform === 'darwin',
		      host: '0.0.0.0',
		      port: 8086, // CHANGE YOUR PORT HERE!
		      https: {
				key  : fs.readFileSync('certs/cert.pem'),
				cert : fs.readFileSync('certs/key.pem')
			  },
		      hotOnly: false,
		    },
       }
       
 好像沒有用, https 可以, 但 chrome 有 warning. 參考這一篇 [請求可被 Chrome 瀏覽器信任的 Web 憑證](https://dotblogs.com.tw/yc421206/2019/05/24/mmc_request_web_certificate_from_ca_server_can_trusted_by_chrome_browser)
![](https://github.com/Charles-Hsu/deepin-env-setup/blob/master/vue-https-warning.png)
 
 ##### 安裝 golang
 
     $ wget https://dl.google.com/go/go1.13.7.linux-amd64.tar.gz
     $ sudo tar -C /usr/local -xzf go1.13.7.linux-amd64.tar.gz
     
##### 安裝 git

    $ sudo apt install git
    

   
