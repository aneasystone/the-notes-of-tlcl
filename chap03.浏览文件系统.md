- 了解 Linux 操作系统中的目录结构
    + LFHS - Linux Filesystem Hierarchy Standard
    + Windows 下每个单独的设备都对应一个独立的树结构，而在 Linux 下只有一个树结构，其他的设备可以被挂载（mount）到树的某个节点上
    + 可以将目录的树型结构类比成一颗倒置的树，最顶部的是树的根（root）

- pwd 命令
    + print working directory - 显示当前目录
    + 当用户第一次进入终端时，默认当前目录为用户的家目录（home directory）

- ls 命令
    + list - 列出一个目录包含的文件及子目录

- cd 命令
    + change the working directory - 更改当前工作目录
    + 命令格式为：`cd pathname`，其中 `pathname` 可以是绝对路径，也可以相对路径
        * 绝对路径：`cd /usr/bin`
        * 相对路径：`cd ../bin` 或者 `cd ./bin`
            - 了解两个特殊符号：`.` 代表当前目录，`..` 代表当前目录的父目录
            - 注意 `./` 可以省略，所以 `cd ./bin` 可以简写为 `cd bin`
    + cd 命令的快捷键
        * `cd` - 将当前工作目录改为家目录
        * `cd -` - 切换到之前的工作目录
        * `cd ~username` - 切换到用户 username 的家目录

- Linux 下的文件注意事项
    + 以 "." 开头的文件为隐藏文件，使用 `ls -a` 才可以看到这些文件
    + Linux 的文件名是区分大小写的
    + Linux 没有文件扩展名（file extension）这样的概念
    + 尽管 Linux 对文件名中的标点符号没有做特别的限制，但是最好只使用 "."、"-"、"_" 这几个标点，尤其重要的是，不要在文件名中使用空格！