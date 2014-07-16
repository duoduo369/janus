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

快捷键
---

* `ctrl + t`  打开一个新的tab, 此时可以接着使用ctrl + d显示可以打开的文件
* `ctrl + h`  走到左边的tab
* `ctrl + i`  走到右边的tab
* `ctrl + p`  commandP 在一个文件夹下递归找文件的时候非常好用
* `\\w`       可以向后快速跳转
* `\\b`       可以向前快速跳转
* `\cc`       注释当前行
* `\cu`       取消当前行注释
* `\rt`       打开右侧的类和方法工具栏，在python,c,c++这些源文件时常用
* `\hs`       当你按下/进行搜索后，搜索的词会高亮显示，按\hs会toggle高亮
* `\n`        打开左侧目录树,再按一次可以关闭

* `tab`       输入模式中按下tab有各种神奇的补全效果，补全有多个词时按下ctrl 按n会往下，按p会往上

* `F4`  粘贴模式，再按一下关闭

    粘贴模式下，你可以从别的地方直接粘贴代码之类的，并且保持代码的格式。
    此模式不支持tab补全什么的，因此粘完后需要赶紧按下F4返回普通模式。

* `gw`  左右两个单词换位置，注意要从左边这个单词开始
* `ul`  打一行=下划线

当使用类似\rt这种指令打开窗口后需要移动窗口

    ctrl+w+w 可以切换窗口
    ctrl+w 离开手指 o 最大话当前窗口,再重复按一次可以在打开之前的窗口
    ctrl+w h 到左边窗口
    ctrl+w l 到右边窗口
    上下移动类似 j l

* `F3`  需要安装coffeescript, 打开file.coffee, 点F3右侧就会显示编译后的js
* `F5`  可以打开当前文件最近一段时间的修改状态，左上角的圈圈可以改回之前状

快速输入

    例如打开*.py 经常输入一些脚本的头什么的， 只要输入#！ 按下tab即可
    其他的快捷输入在文件~/.vim/janus/vim/tools/vim-snippets/snippets中

* `<leader>fef` format the entire file
* `<leader>u` Convert the entire word to uppercace.
* `<leader>l` Convert the entire word to lowercase.
* `<leader>U` Convert the first char of a word to uppercase.
* `<leader>L` Convert the first char of a word to lowercase.
* `<leader>cd` Change the path to the currently active buffer's file.
* `<leader>md` Make the directory of the currently active buffer's file
* `gw` Swap the current word with the one next to it.
* `<leader>tw` Toggle wrap
* `<leader>fc` Finds the next conflict marker (Tested with Git
  conflicted files).

其他janus插件以及快捷键请:help janus

vim相关
---

最新vim配置文件在[my_linux_configs](https://github.com/duoduo369/my_linux_configs) .vimrc.after 文件

vim其他技巧 [kill_issue](https://github.com/duoduo369/skill_issues/tree/master/tools) 下的vim.issue.md
