# rdp_bf
rdp爆破工具，基于freerdp，目前只支持mac（因为使用mac，并且找不到mac下好用的rdp爆破，所以尝试写了一个，之后好用的话可能会编译linux和windows版本），采用多进程的模式，因为经过测试多线程和单个线程爆破次数过多freerdp的库会出现问题，所以采用多进程的方式每个进程只爆破少量密码然后退出，退出后会在新建一个进程继续爆破，直到爆破密码或者密码字典爆破完成。

```
    ____  ____  ____    ____  _____
   /  __\/  _ \/  __\  /  __\/    /
   |  \/|| | \||  \/|  | | //|  __\
   |    /| |_/||  __/  | |_\\| |
   \_/\_\\____/\_/     \____/\_/
   
   --host          Host 支持格式如下：192.168.0.0/24,192.168.0-255.0-255,192.168.0.1-192.168.0.255
   -iL             从文件中输入host（默认为 ./ip.txt）
   -p              Port
   --user          用户名支持格式如下：admin,manager,user
   --uL            从文件中输入用户名（默认为 ./dics/username.txt）
   --pass          密码格式如下：password,123456
   -pL             从文件中输入密码（默认为 ./dics/password.txt）
   -o              输出爆破成功的结果到一个指定的文件中（默认为 ./result.txt）
   --domain        Domain
   -t              Number of hosts blasted at the same time (默认为 5).
   -c              The number of processes that explode rdp at the same time per host (默认为 10).
   -r              Number of retries after blasting error (默认为 3).
   -d              Delay time (ms) (默认为 0)
   --pass-count    Number of passwords blasted per process (默认为 100).
   --proxy         Proxy support format socks5://user:password@ip:port
   --log-level     The value is 1 for all logs, otherwise only successful logs are displayed (默认为 1).
   --delims        Separator for host, user name, and password (默认为 ,).
   -h              Help
```
