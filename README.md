# 3D打印记事本

本人目前正在使用两款打印机：
* 创想三维Ender S1 Pro
* 拓竹P1S-C

主要使用拓竹Bambu Studio切片软件为三维模型生成G-Code

该Repo主要记录切片软件的使用技巧、耗材调参、机器维护与调试等一系列与3D打印相关的内容

--- 

### 🟢 MacOS中BambuStudio的操作方式

| 输入  | 效果  | 说明  |
| --- | --- | --- |
| ⌘ + 双指平移 | 平移画面 | 平移摄像机 |
| 双指移动 | 缩放画面 | 摄像机焦距变大或变小 |
| 单指按压平移 | 旋转画面 | 以屏幕中心为原点旋转画面 |
| ⌘ + 单指按压平移 | 框选  | -   |

---

### 🟢 Shapr3D模型文件导入与Bambu Studio规范流程

个人建议使用：STEP或3MF格式，其次推荐使用STL。

Shapr3d的文件结构如下图所示:

<img src="https://github.com/JpHoooo/3DPrint/assets/42137140/2dd44f91-7576-44e8-929a-563f6c30dedd" width="480px">

则导出为STEP并导入到Bambu Studio，如下图所示:

<img src="https://github.com/JpHoooo/3DPrint/assets/42137140/ef224344-3a08-4400-be80-e468a15d6524" width="480px">

则导出为3MF并导入到Bambu Studio，如下图所示:

<img src="https://github.com/JpHoooo/3DPrint/assets/42137140/be8122b8-653c-45d9-be27-33edbe9544b5" width="480px">

则导出为STL并导入到Bambu Studio并拆分为零件，如下图所示:

<img src="https://github.com/JpHoooo/3DPrint/assets/42137140/55f62567-ff68-42a6-a1ba-35b3d8169044" width="480px">

**结论**
* 对象父物体名称都与Shapr文件名有关
* 对象子物体名称与格式有关
  - STEP：与子文件夹名有关
  - 3MF：与子文件名有关
  - STL：与子文件名和文件夹名无关，拆分出来的名称与父物体名称有关

---

### 🟢 建模公差测试

在层高为0.20mm标准设置中打印模型时，公差半径为0.2mm * 0.24mm

后续解释
  