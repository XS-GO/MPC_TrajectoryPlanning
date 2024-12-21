# **Spatio-Temporal-Trajectory-Planning - 基于时空联合思想的轨迹规划**

## **项目概述**
本项目基于 **MPC_TrajectoryPlanning** 仓库进行扩展，增加了时空联合规划功能，并通过MPC（模型预测控制）对采样轨迹进行优化。原项目使用了横纵向解耦的MPC轨迹规划方法，在单向双车道场景中生成动态和静态障碍物的避障轨迹。

原项目链接：https://github.com/JingyanXing/MPC_TrajectoryPlanning.git

### **改动概述：**
1. 在原项目环境下新增了基于采样的时空联合规划功能。
2. 使用MPC对采样轨迹进行优化，取代了原有的横纵向MPC优化方法。

### **预期实现：**
1. **参考线动态更新：** 参考Openpilot和Apollo框架，在车辆行驶过程中动态更新参考线，考虑自车与障碍物的状态。
2. **横纵向解耦MPC：** 参考Openpilot和Apollo框架，基于简化的车辆运动学建模，采用横纵向解耦MPC轨迹规划方法。
3. **车辆位姿动态显示：** 基于进程通信实时动态显示车辆位姿。

---

## **安装说明**

### **依赖**
确保你的环境中安装了以下依赖：
- CMake
- 编译器：如GCC
- Python环境用于可视化（Python 3+）
- CasADi：用于MPC优化
- Socket通信库

### **安装说明：**
首先克隆本项目到本地：<br>
git clone https://github.com/XS-GO/Spatio-Temporal-Trajectory-Planning.git
在项目Spatio-Temporal-Trajectory-Planning目录下<br>
cd build && cmake .. && make<br>
测试是否安装成功：**./main**<br>
可视化**visualserver**启用方法：令起终端cd进入**visual**目录下， 执行 **python visualserver.py**。可视化服务端唤起，随后在原终端调用可执行文件 <br>

### **后续待更新**
