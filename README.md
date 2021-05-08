# rdp_bf
rdp爆破工具，基于freerdp，目前只支持mac（因为使用mac，并且找不到mac下好用的rdp爆破，所以尝试写了一个，之后好用的话可能会编译linux和windows版本），采用多进程的模式，因为经过测试多线程和单个线程爆破次数过多freerdp的库会出现问题，所以采用多进程的方式每个进程只爆破少量密码然后退出，退出后会在新建一个进程继续爆破，直到爆破密码或者密码字典爆破完成。

```
    ____  ____  ____    ____  _____
   /  __\/  _ \/  __\  /  __\/    /
   |  \/|| | \||  \/|  | | //|  __\
   |    /| |_/||  __/  | |_\\| |
   \_/\_\\____/\_/     \____/\_/
   
   --host          Host address support format 192.168.0.0/24,192.168.0-255.0-255,192.168.0.1-192.168.0.255
   -iL             Enter the host address from the file. (default ./ip.txt)
   -p              Port
   --user          User name support format admin,manager,user
   --uL            Enter the user name from the file (default ./dics/username.txt).
   --pass          Password support format password,123456
   -pL             Enter the password from the file (default ./dics/password.txt).
   -o              Output the blasting result to the given file name (default ./result.txt).
   --domain        Domain
   -t              Number of hosts blasted at the same time (default 5).
   -c              The number of processes that explode rdp at the same time per host (default 10).
   -r              Number of retries after blasting error (default 3).
   -d              Delay time (ms) (default 0)
   --pass-count    Number of passwords blasted per process (default 100).
   --proxy         Proxy support format socks5://user:password@ip:port
   --log-level     The value is 1 for all logs, otherwise only successful logs are displayed (default 1).
   --delims        Separator for host, user name, and password (default ,).
   -h              Help
```
