### 命令的一般格式

一般情况下，命令的格式如下：

```
command -options arguments
```

其中，`-options` 可以是像 `-o` 这样的短格式，也可以是 `--long-options` 这样的长格式。
多个短格式选项也可以合并在一起，如：`-ab` 表示 `-o -b` 。

例子：`ls -lt --reverse`

### ls 命令

- ls - 显示当前目录下的所有文件和子目录
- ls dir1 dir2 ... - 同时显示多个目录
- ls -l - 以长格式输出（long format）

#### ls 命令的常用选项

- `-a, --all` - 显示所有文件，包括隐藏文件
- `-d, --directory` - 默认情况下，ls 命令显示目录下的内容，而不是目录本身，可以使用这个选项和 `-l` 查看指定目录的详细信息
- `-F, --classify` - 在文件名后添加一个标识符来区分不同类型的文件
- `-h, --human-readable` - 将文件大小转换为方便人类阅读的格式，譬如：13.2 MB 这种格式
- `-l` - 以长格式输出
- `-r, --reverse` - 反向显示
- `-S` - 以文件大小排序
- `-t` - 以文件的修改时间排序

#### 长格式

一个长格式的例子如下：

```
-rw-r--r-- 1 root root 3576296 2007-04-03 11:05 Experience ubuntu.ogg
```

每一列代表的意义如下：

- `-rw-r--r--` - 第一个字符代表文件类型（- 表示文件，d 表示目录），后面分别是文件所有者、文件所属组、其他人访问这个文件的权限。
- `1` - 该文件硬链接的个数
- `root` - 文件所有者名称
- `root` - 文件所属组名称
- `3576296` - 文件大小，单位字节
- `2007-04-03 11:05` - 文件的最后修改时间
- `Experience ubuntu.ogg` - 文件名

### file 命令

- 使用 `file filename` 确定文件类型

### less 命令

- 使用 `less filename` 查看文本类型的文件内容
- 了解 `more` 命令 和 `pagers` 程序
- Less is More

#### less 快捷键

- `Page Up or b` - 向上一页
- `Page Down or space` - 向下一页
- `Up Arrow` - 向上一行
- `Down Arrow` - 向下一行
- `G` - 跳到文件结尾
- `1G or g` - 跳到文件开头
- `/charaters` - 搜索
- `n` - 向后搜索下一个
- `h` - 帮助
- `q` - 退出

### Linux Filesystem Hierarchy Standard

- `/` - 根目录
- `/bin` - 包含系统启动时必须的一些程序
- `/boot` - 包含 linux kernel、intial RAM disk image 和 boot loader
    + /boot/grub/grub.conf
    + /boot/grub/menu.lst
    + /boot/vmlinuz
- `/dev` - 包含所有系统识别的设备节点
- `/etc` - 包含所有系统范围内的配置文件
    + /etc/crontab
    + /etc/fstab
    + /etc/passwd
- `/home` - 用户家目录
- `/lib` - 包含系统程序所使用的共享类库
- `/lost+found` 
- `/media` - 可移动设备的自动挂载点
- `/mnt` - 可移动设备的手动挂载点
- `/opt` - 用于安装可选的软件，譬如一些商业程序
- `/proc` - 它是个虚拟文件系统，包含的文件都是系统内核的一些信息
- `/root` - root 用户的家目录
- `/sbin` - 包含一些用于执行关键系统任务的二进制程序
- `/tmp` - 临时文件
- `/usr` - 应该是 Linux 系统下最大的一个目录，包含用户使用的一些常规文件
    + `/usr/bin` 
    + `/usr/lib` 
    + `/usr/local` 
    + `/usr/sbin` 
    + `/usr/share` 
    + `/usr/share/doc` 
- `/var` - 包含一些动态的内容，譬如，数据库、spool 文件、邮件等
    + `/var/log` - 日志文件

### 链接文件

- 硬链接
- 软链接（符号链接）

符号链接文件格式如下，注意第一个字符为 `l`，文件名部分会显示出链接到的真实文件。参考[后面的章节](https://github.com/aneasystone/the-notes-of-tlcl/blob/master/chap05.%E6%93%8D%E4%BD%9C%E6%96%87%E4%BB%B6%E5%92%8C%E7%9B%AE%E5%BD%95.md#创建链接)。

```
lrwxrwxrwx 1 root root 11 2007-08-11 07:34 libc.so.6 -> libc-2.6.so
```