---
layout: post
title:  "linux命令行常用操作"
date:   2020-03-15 14:00:00 +0530
categories: gvim
---
vim命令模式下

:Explore  当前窗口下打开

:Vexplore 竖直分割窗口打开

:Sexplore 水平分割窗口打开

:vsp+file name                  纵向分栏显示

Ctrl+Alt+D                      快速显示桌面

gvim ~/.vimrc                   打开vimrc用户配置文件

:colorscheme peachpuff          设置主题

:set guifont=Monospace\ 15      设置字体大小

mkdir  test                     创建test文件目录

rm -rf + directory name         快速删除目录

cp 文件名 路径  例如：cp  hello.csv  ./python/ml：把当前目录的hello.csv拷贝到当前目的python文件夹里的ml文件夹里

cp 源文件名 新文件名  例如：cp  hello.txt   world.txt：复制并改名,并存放在当前目录下  

cp file1 file2 复制一个文件 

cp dir/* . 复制一个目录下的所有文件到当前工作目录 

cp -a /tmp/dir1 . 复制一个目录到当前工作目录 

cp -a dir1 dir2 复制一个目录 

Vim查找关键字   :/+关键字，回车，如果要继续查找关键字，输入n，向前查找，输入N（大写）

gf（goto file）快速打开包含的头文件 打开包含的头文件并查看头文件包含的内容，可以通过快捷键gf（goto file）完成

解压文件 tar -zxvf archive_name.tar.gz -C new_dir 

打开或编辑.doc .odt等文本文档命令:  openoffice.org -a 文件名.doc &

打开演示文件命令：openoffice.org -g 文件名.... &

打开电子表格： openoffice.org -c 文件名 &

打开pdf文件：    evince 文件名 & 打‘&’的目的是让文件在后台运行，命令行终端还能用。

terminal中输入：acroread vcsmx_ug.pdf 打开VCS user guide

底线命令模式

:0或:1跳到文件第一行

:$跳到文件最后一行

命令模式

gg跳到第一行

shift+g跳到文件最后一行