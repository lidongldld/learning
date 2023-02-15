### 方法一


##### 1、获取github.com可用的dns域名
打开 http://tool.chinaz.com/dns?type=1&host=www.github.com&ip=

##### 2. 在C:WindowsSystem32driversetchosts中加入
 52.74.223.119 www.github.com

##### 3. 然后访问https://github.com/

### 方法二

使用 https://github.com.ipaddress.com/www.github.com 来解析github的服务器ip地址,
根据解析到的ip，将其填写到hosts文件中，再次在浏览器访问github.com即可。
