# ToonURP（刚刚开始）

## Unity版本

 - Unity 2022.3
 - URP14

## 安装使用

在Unity项目的Packages文件夹下运行

```
git clone https://github.com/Reuben-Sun/ToonURP.git
```

并拉新submodule

```
cd ToonURP
git submodule update --init --recursive
```

替换Render Pipeline Assets，使用Setting文件夹下的URP-HighFidelity.asset

![替换资产](Documentation~/image/replace_assets.png)

## 开发计划

- [ ] 基础卡通材质
  - [x] 二值CellShading
  - [x] 多光源
  - [x] 色散
  - [x] SRP batcher
- [x] 边缘检测描边 
- [ ] 人物
  - [ ] 眼睛
  - [ ] 头发
  - [ ] 黑丝
  - [x] 脸
    - [x] SDF阴影
- [ ] 卡通面片草
  - [x] 几何着色器草
  - [ ] HiZ剔除+Instance
  
- [x] 卡通石头
  - [x] 顶部覆盖植被
- [ ] 卡通水
  - [x] 深度采样颜色渐变与法线扰动波纹
  - [ ] 焦散
  - [ ] 反射水面物体
  - [ ] 近海水花
  - [ ] 物体交互
- [ ] 卡通树

## Shader 设计

> 可以参考ToonUnlit.shader的实现

我希望我的Shader是易于扩展的，用户只需要定义一个Shader文件，修改传入的参数，在`PreProcessMaterial`中修改`ToonSurfaceData`，无需要改动Pass里的顶点片元函数，就能快速实现自己的效果



## 参考 

[FernRP](https://github.com/FernRP/FernRPExample)
