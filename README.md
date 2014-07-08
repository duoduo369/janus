Janus 我自己的vim配置
===

一直用[Janus](https://github.com/carlhuda/janus)管理vim,简单完全不用我操心，
这是以前...问题是Janus升级之后，安装是会各种各样的失败，也不知道是不是网络
的问题，而且个人对于vim有一些特殊的配置，因为我是一个pythoner,平时又会写
一些前端，因此空格的问题当时是问题，还有一些习惯的快捷键，我不想每次装机器
的时候都重新搞一次(装机器是经常的事情),因此有了这个东西。

目前所有配置都在**ubuntu**下。

Pre install
---

[Janus Pre install](https://github.com/carlhuda/janus/wiki/Pre-requisites)

    sudo apt-get install ruby-dev rake exuberant-ctags ack-grep

剩下的工作
---

将clone或者下载的项目解压，会发现有`home/duoduo/.vim` (原谅我这个懒人)

    cp -fr home/duoduo/.vim ~/.vim

    ln -s ~/.vim/janus/vim/vimrc ~/.vimrc
    cp ~/.vim/config/.vimrc.after ~/.vimrc.after

done
