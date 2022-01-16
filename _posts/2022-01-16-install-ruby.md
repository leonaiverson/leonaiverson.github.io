# 安装Ruby
## 安装ruby

ruby可用于安装jekyll，jekyll可用于静态网格的预览。ruby是基于msys2实现的，集成了mingw,为了防止一台电脑里有多个版本的mingw，可将此库作为例如clion的编译工具链使用。

### 安装
1.	下载ruby+devkit
2.	等待安装完成，提示ridk install，并通过
3.	输入1，2，3；
4.	等待安装结束
### 测试
1. 输入gem -v
## 安装jekyll
### 安装
1. 使用 start command promp with ruby
2. 输入gem install jekyll
注意： 不适用ruby 会提示jekyll 安装失败
### 测试
1. 使用 start command prompt with ruby
2. 输入 jekylll -v
### 启动
1. jekyll serve --watch
2. 默认 http://127.0.0.1:4000
3. Q&A
	- 遇到了bundle sassc 版本不兼容  使用bundle update
	- 提示 wdm  使用gem install wdm
	- 提示  cannot load such file -- webrick 因为ruby3.0 不再捆绑webrick 故要[bundle add webrick](https://stackoverflow.com/questions/65617143/cannot-load-such-file-webrick-httputils)
## Clion配置
ruby安装了msys2，msys2里集成了MingW，clion可利用此MingW进行编译。但是ruby里默认没有安装mingw-w64-x86_64-toolchain，故要手动按钻过。
1.	找到pacman所在目录；
2.	在当前目录启动cmd，或者启动cmd,然后进入此目录；
3.	输入 pacman -S mingw-w64-x86_64-toolchain ，等待安装完成
4.	在clion的toolchain 里选择ruby->msys2->mingw64目录。