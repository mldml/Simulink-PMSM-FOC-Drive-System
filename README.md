
基于MATLAB/Simulink 搭建并调试底层双电机控制模型
# 双电机容错控制模型（Simulink）

## 项目简介
本项目基于MATLAB/Simulink搭建双永磁同步电机（PMSM）底层控制模型，实现电机FOC矢量控制、转矩闭环调节及故障容错策略验证，可用于线控转向/电驱系统的算法开发与仿真验证。

## 模型文件说明
- `jianhua_PMSM_FOC.slx`：单电机FOC矢量控制基础模型（含SVPWM、电流环/速度环PI控制）
- `DualMotor_FaultTolerant_TorqueControl.slx`：双电机转矩协同控制模型
- `DualMotor_FaultTolerant_Stateflow.slx`：基于Stateflow的故障诊断与容错控制逻辑
- `DualMotor_FaultTolerant_Healthypoint.slx`：电机健康状态监测与容错切换验证模型

## 关键技术与实现
1.  电机控制：实现永磁同步电机FOC矢量控制，支持SVPWM调制与电流/速度双闭环控制
2.  双机协同：双电机转矩同步分配与偏差补偿，提升系统响应一致性
3.  故障容错：通过Stateflow实现单电机故障检测、降功率运行与冗余切换逻辑
4.  仿真验证：完成阶跃转矩/速度响应测试、故障注入测试，验证控制算法的稳定性与鲁棒性

## 运行环境
- MATLAB/Simulink 版本： R2025a
- 依赖工具箱：Simulink Control Design、Motor Control Blockset
