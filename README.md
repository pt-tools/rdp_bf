# rdp_bf
rdp爆破工具，基于freerdp，目前只支持mac（因为使用mac，并且找不到mac下好用的rdp爆破，所以尝试写了一个，之后好用的话可能会编译linux和windows版本），采用多进程的模式，支持代理，因为经过测试多线程和单个线程爆破次数过多freerdp的库会出现问题，所以采用多进程的方式每个进程只爆破少量密码然后退出，退出后会在新建一个进程继续爆破，直到爆破出密码或者密码字典爆破完成。

```
    ____  ____  ____    ____  _____
   /  __\/  _ \/  __\  /  __\/    /
   |  \/|| | \||  \/|  | | //|  __\
   |    /| |_/||  __/  | |_\\| |
   \_/\_\\____/\_/     \____/\_/
   
   --host          Host 支持格式为 192.168.0.0/24,192.168.0-255.0-255,192.168.0.1-192.168.0.255
   -iL             从文件中输入host（默认为 ./ip.txt）
   -p              Port
   --user          用户名支持格式为 admin,manager,user
   --uL            从文件中输入用户名（默认为 ./dics/username.txt）
   --pass          密码格式为 password,123456
   -pL             从文件中输入密码（默认为 ./dics/password.txt）
   -o              输出爆破成功的结果到一个指定的文件中（默认为 ./result.txt）
   --domain        Domain
   -t              同时爆破多少个host（默认为 5）
   -c              每个host同时有几个进程进行爆破（默认为 10）
   -r              每个密码爆破出错重试的次数（默认为 3）
   -d              爆破的延时 (ms) （默认为 0）
   --pass-count    每个进程一次爆破多少个密码 （默认为 100）
   --proxy         代理支持格式为 socks5://user:password@ip:port
   --log-level     日志显示设置，值为1表示都显示，不为1表示只显示爆破成功的结果（默认为 1）
   --delims        --host、--user和--pass参数的分隔符 （默认为 ,）
   -h              帮助
```
（本人编程水平有限，程序比较简单，希望大家多多支持，程序有什么问题请帮忙指出）
