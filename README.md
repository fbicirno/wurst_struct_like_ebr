# wurst_struct_like_ebr
类似EBR地图的文件结构，地图来自   [EBR map](**https://github.com/Frotty/EBR**)

该项目是为了提供wurst脚本文件的结构规范，不能运行和编译

请看wurst文件夹的内容

Imitation of the file structure of the EBR map, map from [EBR map]
This project is intended to provide structural specifications for wurst script files that cannot be run and compiled
See the contents of the wurst folder

> e.g. I have no time to write english version, if u need that, just contact me.

# 项目结构说明

## lib

核心要素

- 开源系统包——**一个单独存在的系统，提供了扩展功能的函数**
  							例如：Camera Shake System,CustomBar
    							可提供类或函数，单一脚本 跨地图通用
- jass扩展——读取jass函数，以便调用

## map

**集中管理 **初始化，管理地图调用顺序

尽量把init函数放入其中

地图初始化设定——例如任务，建筑位置

**集中管理 **常量，对地图的id，迭代器，颜色，枚举  进行设定

仅放入不更改的常量

注册实体数据——**定义类使其存储实体数据，扩展某些实体**
                               例如：地形，区域，多面板

**集中管理 **功能性的obj对象，写他们特有的方法，然后用物编生成。

注意：要区分不同种类的物编对象


对玩家分类，定义玩家可操作的函数内容

存档函数可以在此制作，可区分存档，设置开关，实现多平台发布。


自定义gui界面，与系统交互

写一些地图专用的系统

complite

定义一些编译时专用的函数，还有自定义注解

地图种子，设定一些地图开关和参数，方便平衡和测试

## update
更新补丁，将增量内容放入其中注册，不改变基类，更安全

