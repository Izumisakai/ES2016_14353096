- ##Cartographer

	- ###Cartographer介绍
	在内部使用了两年之后，谷歌终于宣布开源其制图工具Cartographer， 该技术利用同步定位与制图技术(SLAM)绘制室内建筑平面图，能同时用于二维与三维空间的移动映射。同时，开源 Cartographer 还搭配有开源机器人操作系统(ROS)，使得该技术库更易于部署机器人、无人驾驶、无人机等系统。
	
	- ###Cartographer安装步骤
	
		- ####1、安装ceres solver
				git clone https://github.com/hitcm/ceres-solver-1.11.0.git
				cd ceres-solver-1.11.0/build
				cmake ..
				make –j
				sudo make install     
				
		- ####2、然后安装 cartographer
				git clone https://github.com/hitcm/cartographer.git
				cd cartographer/build
				cmake .. -G Ninja
				ninja
				ninja test
				sudo ninja install
				
		- ####3、安装cartographer_ros
				git clone https://github.com/hitcm/cartographer_ros.git
				cd到catkin_ws目录下运行catkin_make
		
		- ####4、下载数据并launch文件
				roslaunch cartographer_ros demo_backpack_2d.launch bag_filename:=${HOME}/Downloads/cartographer_paper_deutsches_museum.bag
				roslaunch cartographer_ros demo_backpack_3d.launch bag_filename:=${HOME}/Downloads/cartographer_3d_deutsches_museum.bag
				
	- ###实验截图
		- ####2d
		<div align="center"><img src="https://github.com/Izumisakai/ES2016_14353096/blob/master/image/cart1.png" width="75%",height="75%"></div>
		
		- ####3d
		<div align="center"><img src="https://github.com/Izumisakai/ES2016_14353096/blob/master/image/cart2.png" width="75%",height="75%"></div>
		
	- ###实验感想
	这次实验是让我们了解一下ROS的玩法，并且为我们提出了具体的cartographer，这个是一个google的开源项目，目的是用于环境绘图，可以嵌入于机器人中使用，是一个挺牛逼的玩意，我们这个实验也是看一下其绘制2d和3d图片的效果。但是因为才学疏浅，不太能弄懂其中的奥秘。