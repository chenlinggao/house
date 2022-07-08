# Windows



# ==Linux==

#  基本应用

## 1. 指令汇总

（`Ctrl + Alt + T` 打开 `terminal`）

### 1.1. 文件列表

```bash
ls （-l)/(-ld)								//列出当前工作目录下的文件，-l可以显示详情
cd											//切换当前工作目录
pwd											//查看当前工作目录
												其中~表示用户目录，即/home/user(你的用户名)；
												.表示当前目录;
												..表示上一级目录;
touch 文件									//创建文件
gedit 文件									//打开文件，但是我的貌似有点问题，总是弹出连接已关闭什么的。。。看别人的好像没毛病
mkdir (-p) 目录								//创建文件夹,加-p表示可以将路径的层次目录全部创建
rmdir 目录									//删除文件夹，若目录非空，则删除失败
rm -rf 文件或目录							//删除文件或目录，-r表示递归，-f表示强制
rm -rf /*									//删库跑路
cp -rf example example2						//复制文件或目录
mv example example2							//重命名
mv 文件或目录（目标路径） 文件或目录（被移动路径)		//移动文件或目录
```

### 1.2. 归档压缩

```bash
tar -cvf example.tar example ...			//c表示create,v表示verbose，f表示file,可多个打包
tar -xvf example.tar (-C 目录）				//-C(大写）参数指定目标目录，默认是到当前目录
以上两条，-czvf和-xzvf表示顺便压缩或解压缩一下，若是压缩文件后缀为tar.gz
```

### 1.3. 用户与用户组

```bash
sudo passwd root							//初次使用，要设置密码
su （root）									//切换到root用户（后续操作可以不用加sudo了），切换到别的用户只需把后面的root改下就好了
exit										//退出
# -------------------------------------------------
sudo adduser  test1							//添加一个用户，sudo表示以管理员身份运行。
sudo useradd (-m) test1						//useradd同样可以添加用户，但是不会创建用户目录，不过你可以加上-m表示添加一个目录，但是还得另外设置密码，比较麻烦，不如直接adduser来得方便。
sudo passwd test1							//修改密码
sudo userdel test1							//删除用户(删除时记得删除用户目录）
注意：只有特殊用户才能执行sudo，比如你创建的用户test1不行，不信你试试，会提示你不是sudoer。
# -------------------------------------------------
groupadd boys								//创建组
useradd -m -g boys xiaoming					//-g表示主要组，表示添加一个用户，并把他的主要组改为boys。
usermod -g boys xiaoming					//修改已有用户的主要组，但你创建时留下的xiaoming的同名组还会存在
cat /etc/group								//表示查看所有的组，前面一些乱七八糟的暂时不了解，自己创建的主要在后边
cat /etc/passwd								//表示查看所有的用户
-g 表示主要组，你也可以用-G表示次要组，实现一个用户在多个组里
```

### 1.4. 修改文件权限

当我们使用`ls -l 目录`的时候，可以看到前面一大串一大串的`-rwxrwxrwx`。
其中：r表示可读，w表示可写，x表示可执行（对于目录来说，能打开就是可执行）,第一组表示自己，第二组表示同组，第三组表示别人。紧接着的第一个是**文件属主**，第二个是文件的**用户属组**。因此，u表示用户属主，g表示用户属组，o表示除文件属主外的其他人。

```bash
chmod o+w simple							//表示给别人增加文件权限，o表示别人。
chmod o-w simple							//给别人减去可写权限
chomd a+(-)w simple							//a 表示all,表示给所有人增添可写权限
chomd u+(-)w simple							//u表示用户自己（文件属主）
（若a,o,u省略则表示给u和g增添权限）
```

## 2. 安装文件

### 2.1. 从压缩包 

```
# 安装
sudo apt-get install package
sudo dpkg -i package			# 对应deb文件
# 卸载
sudo apt --purge remove software
# 关于依赖问题
sudo apt-get -f install

```



## 3.查看系统消息

### 3.1. 关于磁盘：

#### 3.1.1. 查看磁盘

1. `df -T`       ---- 查看**已挂载**的磁盘信息(磁盘格式类型,  挂载点,  使用率)
2. `fdisk -l` ---- 查看所有挂载或未挂载的磁盘分区,  不显示磁盘格式类型
3. `df -h`        ---- 查看已挂载的盘
4. `lsblk -f`  ---- 

----

# Docker

## 从容器中拷贝文件到宿主机

```bash
sudo docker ps -a     # 获取container_id
sudo docker inspect '{{.Id}}' [上面获取的container_id]  # 以获取id的完整id
sudo docker cp [完整id:所想拷贝的路径] [目标路径]
```



# 装机

## 1. 换源(加速安装)

### 1.1. code

```bash
sudo cp /etc/apt/source.list /etc/apt/source.list.bak
sudo vim /etc/apt/source.list
sudo apt-get update

# Tips:
# 1. 找对应版本的源
# 2. 如果出现依赖问题sudo apt-get -f install
```

### 1.2. 源 --- 可以去找网址的源

```
# 清华
https://mirrors.tuna.tsinghua.edu.cn/help/ubuntu/
# 阿里
https://developer.aliyun.com/mirror/
```

### 1.3. 加速连github

```
sudo vim /etc/hosts

140.82.113.3 github.com
185.199.108.154 github.githubassets.com
185.199.109.154 github.githubassets.com
185.199.110.154 github.githubassets.com
185.199.111.154 github.githubassets.com
185.199.108.154 github.githubassets.com
185.199.109.154 github.githubassets.com
185.199.110.154 github.githubassets.com
185.199.111.154 github.githubassets.com
199.232.68.133 camo.githubusercontent.com
199.232.68.133 camo.githubusercontent.com
199.232.68.133 github.map.fastly.net
199.232.68.133 github.map.fastly.net
199.232.69.194 github.global.ssl.fastly.net
199.232.69.194 github.global.ssl.fastly.net
140.82.113.5 api.github.com
140.82.113.5 api.github.com
199.232.68.133 raw.githubusercontent.com
199.232.68.133 raw.githubusercontent.com
199.232.68.133 user-images.githubusercontent.com
199.232.68.133 user-images.githubusercontent.com
199.232.68.133 favicons.githubusercontent.com
199.232.68.133 favicons.githubusercontent.com
```



## 2. 安装[zsh](https://blog.csdn.net/amoscykl/article/details/80616873)

```bash
cat /etc/shells 	# 查看可用的shell

wget https://gitee.com/mirrors/oh-my-zsh/raw/master/tools/install.sh
vim install.sh

# 修改install.sh

# Default settings
ZSH=${ZSH:-~/.oh-my-zsh}
REPO=${REPO:-ohmyzsh/ohmyzsh} 	# 替换成 REPO=${REPO:-ohmyzsh/ohmyzsh}
REMOTE=${REMOTE:-https://github.com/${REPO}.git}	# 替换成 REMOTE=${REMOTE:-https://github.com/${REPO}.git}
BRANCH=${BRANCH:-master}
```

```
# 更新oh-my-zsh/修改仓库地址
cd ~/.oh-my-zsh
git remote set-url origin https://gitee.com/mirrors/oh-my-zsh.git
git pull
```

### 插件：

#### 1. 自动补全

```
git clone git://github.com/zsh-users/zsh-autosuggestions $ZSH_CUSTOM/plugins/zsh-autosuggestions
source .
```



## n. 可能遇到的问题

### 2.1. 问题：连上有线网线后，无有线图标

#### 1. 查看网卡与其驱动是否匹配

```
lspci | grep net # 查看网卡型号, Ethernet controller:后的部分为网卡型号
lspci -k 		 # 查看网卡驱动, 找到Ethernet相关的行, Kernel driver显示的是驱动信息
```

#### 2. 删除旧驱动

```
modinfo r8169 | grep filename		  # 查看驱动文件所在的位置，其中的r8169请自行替换为自己的网卡驱动名称。
mv path/r8169.ko path/r8169.ko.backup # 其中的path请用上一步查找到的文件路径替换
rm path/r8169.ko 					  # 直接删除
rmmod r8169							  # 卸载驱动
lsmod | grep r8169					  # 无显示或者显示结果没有r8169则表明删除成功
```

#### 3. 下载新驱动并挂载在相对应网卡官网上下载驱动

**使用DKMS安装驱动**

`sudo apt-get install dkms`

`sudo tar xvf r8125-9.004.01.tar.bz2 -C /usr/src`

`touch /usr/src/r8125-9.004.01/dkms.conf` # 在/use/src的对应文件夹中创建一个新文件，名称为dkms.conf，比如我这里就要在/usr/src/r8125-9.004.01中创建。

`sudo vim /usr/src/r8125-9.004.01/dkms.conf`	# dkms.conf中输入以下内容(换成对应的驱动和版本)：

```
PACKAGE_NAME=Realtek_r8125
PACKAGE_VERSION=9.004.01 
DEST_MODULE_LOCATION=/updates/dkms
BUILT_MODULE_NAME=r8125
BUILT_MODULE_LOCATION=src/
MAKE="'make' -C src/ all"
CLEAN="'make' -C src/ clean"
AUTOINSTALL="yes"
```

```
# 编译DKMS并挂载驱动
sudo dkms add -m r8125 -v 9.004.01
sudo dkms build -m r8125 -v 9.004.01
sudo dkms install -m r8125 -v 9.004.01
sudo depmod -a
sudo modprobe r8125 #挂载驱动
# 查看驱动是否安装成功
lspci -k 
```



### 2.2. Ubuntu20.04安装NVIDIA显卡驱动+cuda+cudnn配置

#### 1. 查看显卡型号，在NVIDIA下对应驱动

```
# 卸载Ubuntu自带的驱动
sudo apt purge nvidia*
# 禁用nouveau nvidia驱动
sudo vim /etc/modprobe.d/blacklist.conf
# 加入以下内容：

blacklist nouveau
options nouveau modeset=0

# 更新
sudo update-initramfs -u
# 重启、查看是否屏蔽
sudo reboot
lsmod | grep nouveau # 无显示即成功
```

```
# 装NVIDIA驱动

sudo service lightdm stop
sudo apt install -y lightdm # 如果上一步报错就安装lightdm 
# 进入serve界面(Ctel+Alt+F1/F2)
sudo passwd root# 设置root密码(一般都设置好了)

gcc --version # 查看是否安装了gcc
sudo apt-get install gcc & make # 如果没安装，同时安装gcc和make

# cd到显卡驱动的目录
sudo chmod a+x NVIDIA-Linux-x86_64-450.80.02.run
sudo ./NVIDIA-Linux-x86_64-450.80.02.run -no-x-check -no-nouveau-check -no-opengl-files
    # -no-x-check:安装时关闭X服务
    # -no-nouveau-check: 安装时禁用nouveau
    # -no-opengl-files:只安装驱动文件，不安装OpenGL文件
```

下面者两个按图中选择，其他默认就好

![image.png](T:\img_typora\image-aab9f3d76fbe4c7293696e3dcb3c1b2b.png)![image.png](T:\img_typora\image-3629793f1cfa4ce096618e978b908577.png)

`nvidia-smi` # 如果能显示即安装成功，并查看CUDA版本

#### 2. 装cuda

```
# cd到所在目录
# 安装cuda
sudo sh cuda_11.0.2_450.51.05_linux.run
```

<img src="T:\img_typora\image-97e533d2efd4405d80b04b4a6fb1169a.png" alt="image.png"  /><img src="T:\img_typora\image-d4c17663fd4d4bedb781493d45dc171d.png" alt="image.png"  />

结果：

<img src="T:\img_typora\image-83941874dc274b51a9e401c2e6ee3b23.png" alt="image.png"  />

```
# 配置环境变量
vim ~/.bashrc
# 将下面的11.0替换为你的cuda版本，其他不变，如果不知道自己安装的是哪个版本，就去/usr/local/文件夹下找一下
export PATH=/usr/local/cuda-11.0/bin${PATH:+:${PATH}}
export LD_LIBRARY_PATH=/usr/local/cuda-11.0/lib64${LD_LIBRARY_PATH:+:${LD_LIBRARY_PATH}}

# 执行如下命令更新变量，使其生效
source ~/.bashrc
nvcc -V
```

即完成

<img src="T:\img_typora\image-66cd14a41c004a6097459d9352f19f10.png" alt="image.png"  />

#### cudnn安装([下载链接](https://developer.nvidia.com/rdp/cudnn-download))

```
# cd对应文件夹下
sudo cp cuda/include/cudnn.h /usr/local/cuda/include/
sudo cp cuda/lib64/libcudnn* /usr/local/cuda/lib64/
# 赋予文件执行权限
sudo chmod a+r /usr/local/cuda/include/cudnn.h
sudo chmod a+r /usr/local/cuda/lib64/libcudnn*
```

#### CUDA测试

```
# cd到/home/用户名/NVIDIA_CUDA-11.0_Samples
make

# cd到/home/用户名/NVIDIA_CUDA-11.0_Samples//1_Utilities/deviceQuery
./deviceQuery

# cd到NVIDIA_CUDA-11.0_Samples/1_Utilities/bandwidthTest
./bandwidthTest
```

### 磁盘挂载

#### 1. 正常过程

```bash
# 将磁盘挂载成一个文件夹
sudo fdisk -l(df -h , lsblk)# 查看硬盘状况, 能看到多块物理磁盘/dev/sda, /dev/sdb ...(假设sdb为挂载)
sudo fdisk /dev/sdb			# 进入对sdb磁盘的设置界面
-d 							# 删除分区
-q 							# 退出
mkfs.ext4 /dev/sdb			# 将磁盘转换成ext4文件系统
sudo mkdir /home/data		# 创建文件夹
mount /dev/sdb /home/data	# 将sdb挂载到data上

umount /home/data			# 取消挂载，/home/data是挂载点
```

#### 2. 问题：

##### 2.1. 不能取消挂载

* 出现类似“umount: /mnt: target is busy.”等字样，该报错通常是由于待卸载磁盘正在使用，导致无法直接卸载。需要将当前使用数据盘的进程杀掉，才能卸载。

  ```bash
  # 查看占用挂载点的进程
  
  ```

  

### 权限

```
sudo chmod -R 777 file_dir  # 任何人都能进行读写
```

