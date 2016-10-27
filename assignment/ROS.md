- ##ROS(Robot Operating System)

- ###ROS介绍

	- ####ROS（机器人操作系统，Robot Operating System），是专为机器人软件开发所设计出来的一套电脑操作系统架构。它是一个开源的元级操作系统（后操作系统），提供类似于操作系统的服务，包括硬件抽象描述、底层驱动程序管理、共用功能的执行、程序间消息传递、程序发行包管理，它也提供一些工具和库用于获取、建立、编写和执行多机融合的程序。

	- ####ROS的运行架构是一种使用ROS通信模块实现模块间P2P的松耦合的网络连接的处理架构，它执行若干种类型的通讯，包括基于服务的同步RPC（远程过程调用）通讯、基于Topic的异步数据流通讯，还有参数服务器上的数据存储。

- ###ROS安装(基于Ubuntu)

	- ####Installation
		- #####Configure your Ubuntu repositories

		- #####Setup your sources.list
				sudo sh -c 'echo "deb http://packages.ros.org/ros/ubuntu $(lsb_release -sc) main" > /etc/apt/sources.list.d/ros-latest.list'

		- #####Set up your keys
				sudo apt-key adv --keyserver hkp://ha.pool.sks-keyservers.net:80 --recv-key 0xB01FA116

		- #####Installation
				sudo apt-get update
				sudo apt-get install ros-jade-desktop-full

		- #####Initialize rosdep
				sudo rosdep init
				rosdep update

		- #####Environment setup
				echo "source /opt/ros/jade/setup.bash" >> ~/.bashrc
				source ~/.bashrc

		- #####Getting rosinstall
				sudo apt-get install python-rosinstall

- ###实验体会

	- ####这次的实验内容只是单纯的在ubuntu上配置ros，为下一次的实验做准备，总体比较简单，照着网站上的教程一步步走，并没有遇到问题。
