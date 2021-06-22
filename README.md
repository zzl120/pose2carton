# Pose2Carton 

EE228 课程大作业 利用3D骨架控制3D卡通人物 (https://github.com/yuzhenbo/pose2carton) 

数据组别： 21

数据类型： 12组匹配 + 4组蒙皮 


# Maya 环境配置

1、申请一个autodesk账户并申请教育版权限，然后获得maya2020安装包的链接，安装maya2020。  

2、将maya2020安装目录的bin文件夹的路径添加到环境变量。  

3、打开cmd，输入mayapy，安装pip，numpy。


# 匹配流程
挑选合适的模型，在transfer.py中，在最后函数的参数部分改为自己选中模型序号的txt文件，然后运行。运行后可以获得关节点名称和对应的序号，然后将得到的模型的关节点索引与提供的人体SMPL关节点索引进行匹配。匹配时要保证两者的核心拓扑结构尽可能一样，即核心骨骼点要匹配上。在索引关系匹配好之后，再次运行transfer.py，然后运行vis.py，就可以得到可视化的图片和视频。  

对于从网上下载fbx模型，需要先通过fbx_parser.py进行解析，解析成功后会得到xxx.fbx、xxx.obj、xxx.txt、xxx_intermediate.mtl,
xxx_intermediate.obj文件和xxx.fbm文件夹。运行完tranfer.py后会得到一个名叫obj_seq_5_3dmodel的文件夹，将之前解析得到的mtl文件和fbm文件移入此文件夹中，并将mtl中指向贴图的绝对路径改为相对路径。




# 新增脚本说明

主要是对cv2.Videowriter()的参数进行修改，对vis.py的具体修改如下所示：  

save_video_path = osp.join(savedir, "vis.avi")  

 h, w = 1050, 1920  
 
 video_writer = cv2.VideoWriter(save_video_path,cv2.VideoWriter_fourcc('I','4','2','0'), 24, (w, h))




# 项目结果


![image](/img/16.png)



# 协议 
本项目在 Apache-2.0 协议下开源

所涉及代码及数据的所有权以及最终解释权归倪冰冰老师课题组所有. 
