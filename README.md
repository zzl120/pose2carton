# Pose2Carton 

EE228 课程大作业 利用3D骨架控制3D卡通人物 (https://github.com/yuzhenbo/pose2carton) 

数据组别： 21

数据类型： 12组匹配 + 4组蒙皮 


# Maya 环境配置

1、申请一个autodesk账户并申请教育版权限，然后获得maya2020安装包的链接，安装maya2020。
2、将maya2020安装目录的bin文件夹的路径添加到环境变量。
3、打开cmd，输入mayapy，安装pip，numpy。


# 匹配流程

xxx (这里请简单描述你熟悉/使用 匹配代码的流程，可以简述对代码的理解/各个函数作用等。)



# 新增脚本说明

主要是对cv2.Videowriter()的参数进行修改，对vis.py的具体修改如下所示：
save_video_path = osp.join(savedir, "vis.avi")
 h, w = 1050, 1920
    video_writer = cv2.VideoWriter(save_video_path,cv2.VideoWriter_fourcc('I','4','2','0'), 24, (w, h))




# 项目结果

xxx. (这里放置来自你最终匹配结果的截图， 如

![image](../img/pose2carton.png))



# 协议 
本项目在 Apache-2.0 协议下开源

所涉及代码及数据的所有权以及最终解释权归倪冰冰老师课题组所有. 
