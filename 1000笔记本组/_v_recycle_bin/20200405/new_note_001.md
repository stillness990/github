# new_note
简单介绍一下Ubuntu的apt-get几个指令
```
apt-get clean:
```
apt-get安装的软件包会存储在/var/cache/apt/archives/和/var/cache/apt/archives/partial/两个目录下，长期使用会占用硬盘空间。clean指令就是删除掉这两个目录中的软件包，除了已经被锁定的文件。
```
apt-get autoclean:
```
同样是这两个目录下的软件包，不同的是autoclean只删除不能被再次下载的软件包，所以说apt-get clean删除清理更彻底。autoclean的官方定义：
>autoclean
Like clean, autoclean clears out the local repository of retrieved package files. The difference is that it only removes package files that can no longer be downloaded, and are largely useless. This allows a cache to be maintained over a long period without it growing out of control. The configuration option APT::Clean-Installed will prevent installed packages from being erased if it is set to off.
```
apt-get remove:
```
删除（卸载）已经安装的软件包（保留相关文件）。
```
apt-get --purge remove:
```
完全卸载软件，包括相关的配置文件。
```
apt-get autoremove:
```
自动卸载软件，及其有依赖相关的软件包；和一些Ubuntu认为不常用的软件包。。。这个命令使用要小心
我个人理解，通常情况下为保证系统整洁，完全卸载某软件：
```
apt-get --purge remove [packagenames]
```
如果系统功能单一，不用做生活工作用机（比如跑邮件代理、个人建站之类的），在清理安装包时可以使用；亦或者自己对安装的软件包依赖非常熟悉了解时，也可以使用，反之系统容易出问题。
```
apt-get autoremove [packagenames]
```