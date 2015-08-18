- 什么是命令行（command line）？
    + command line == shell
    + bash - Bourne Again SHell
    + 在 GUI 环境下使用终端模拟 shell
        * terminal emulator
        * KDE: konsole, GNOME: gnome-terminal

- 命令提示符的一般格式：`[用户名@机器名 当前目录]$` ，最后一个字符也有可能是 `#` ，代表有 root 权限。

- 使用键盘的上下键访问命令的历史，默认情况下 Linux 保存最近的 500 条命令。
- 使用键盘的左右键编辑命令。

- X Window System 具有一种快速复制粘贴的功能：使用鼠标选择一段文本，然后单击鼠标中键即可复制并粘贴该文本。

- 注意不要使用 Ctrl-c 和 Ctrl-v 来复制粘贴。

- 了解窗口的聚焦策略（focus policy）
    + click to focus
    + focus follows mouse

- 开始尝试一些简单命令：
    + date - 显示系统当前时间和日期
    + cal - 显示当前月份的日历
    + df - 查看磁盘剩余空间
    + free - 显示空闲内存的数量

- 关闭终端的窗口或使用 exit 命令退出终端程序

- 如果系统上没有终端程序可用，可以使用虚拟终端（virtual terminal or virtual console）
    + 一共有 6 个虚拟终端运行在后台，可以使用快捷键 Ctrl-Alt-F1 ~ Ctrl-Alt-F6 访问
    + 使用快捷键 Alt-F1 ~ Alt-F6 在虚拟终端之间切换
    + 使用快捷键 Alt-F7 回到桌面环境