# VMware14 虚拟机安装MAC OS 13
## 准备工作
- VMware Workstation Pro 14
- Mac OS 10.13镜像
- Unlocker v3.0.0
```
链接：
```
## 安装步骤
- VMware14 安装直接继续下一步即可，许可证激活密钥百度即可
- VMWare 安装完成后，打开任务管理器：win+R，输入 services.msc，将关于 VMware 的服务全部停止运行 

![image](https://github.com/zmlwzx/zmlwzx.github.com/blob/master/images/VMware/服务.jpg)

- (MAC 补丁):解压 Unlocker 文件，右键选择以管理员身份运行，等待运行完
```
注意：为什么需要Unlocker？
官方原版VMware是不支持MAC OS安装的,所以需要Unlocker工具。
```

![image](https://github.com/zmlwzx/zmlwzx.github.com/blob/master/images/VMware/unlocker-1.jpg)
![image](https://github.com/zmlwzx/zmlwzx.github.com/blob/master/images/VMware/unlocker-2.jpg)

---
## VMware 创建 Mac 虚拟机
1. 打开VMware 14，创建新的虚拟机，此处安装了典型（推荐）下的配置类型，下一步

![image](https://github.com/zmlwzx/zmlwzx.github.com/blob/master/images/VMware/界面.jpg)
![image](https://github.com/zmlwzx/zmlwzx.github.com/blob/master/images/VMware/1.png)

2. 选择程序光盘映像文件，选择下载好的10.13.cdr文件

![image](https://github.com/zmlwzx/zmlwzx.github.com/blob/master/images/VMware/2.png)

3. 选择 Mac 操作系统及版本

```
注意：此处会显示Apple Mac OS X(M)就是因为运行了Unlocker v3.0.0，如果没有此选项，需再次运行
```
![image](https://github.com/zmlwzx/zmlwzx.github.com/blob/master/images/VMware/3.png)

4. 创建虚拟机名称

![image](https://github.com/zmlwzx/zmlwzx.github.com/blob/master/images/VMware/4.png)

5. 此处都是默认安装

![image](https://github.com/zmlwzx/zmlwzx.github.com/blob/master/images/VMware/5.png)

6. “自定义硬件”可根据自己的需求进行配置，本人没有配置

![image](https://github.com/zmlwzx/zmlwzx.github.com/blob/master/images/VMware/6.png)
---

## Mac 系统配置
---
1. 此时发现有如下报错，需要修改Mac-10.vmx(虚拟机名称)文件，编辑VMX文件，在 smc.present = "TRUE" 后面添加了 smc.version = 0,保存退出,重新启动客户机，出现下面你的界面

![image](https://github.com/zmlwzx/zmlwzx.github.com/blob/master/images/VMware/7.png)
![image](https://github.com/zmlwzx/zmlwzx.github.com/blob/master/images/VMware/8.png)
![image](https://github.com/zmlwzx/zmlwzx.github.com/blob/master/images/VMware/9.png)


2. 系统安装
- 进入语言选择界面，本人选择的自然是中文简体.



---


