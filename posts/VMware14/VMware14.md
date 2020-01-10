# VMware14 虚拟机安装MAC OS 13
## 准备工作
- VMware Workstation Pro 14
- Mac OS 10.13镜像
- Unlocker v3.0.0
- Vmware Tools
```
链接：
```
## 安装步骤
- VMware14 安装直接继续下一步即可，许可证激活密钥百度即可
- VMWare 安装完成后，打开任务管理器：win+R，输入 services.msc，将关于 VMware 的服务全部停止运行 

![image](https://zmlwzx.github.io/images/VMware/服务.jpg)

- (MAC 补丁):解压 Unlocker 文件，右键选择以管理员身份运行，等待运行完
```
注意：为什么需要Unlocker？
官方原版VMware是不支持MAC OS安装的,所以需要Unlocker工具。
```

![image](https://zmlwzx.github.io/images/VMware/unlocker-1.jpg)
![image](https://zmlwzx.github.io/images/VMware/unlocker-2.jpg)
---
## VMware 创建 Mac 虚拟机
1. 打开VMware 14，创建新的虚拟机，此处安装了典型（推荐）下的配置类型，下一步

![image](https://zmlwzx.github.io/images/VMware/界面.jpg)
![image](https://zmlwzx.github.io/images/VMware/1.png)

2. 选择程序光盘映像文件，选择下载好的10.13.cdr文件

![image](https://zmlwzx.github.io/images/VMware/2.png)

3. 选择 Mac 操作系统及版本

```
注意：此处会显示Apple Mac OS X(M)就是因为运行了Unlocker v3.0.0，如果没有此选项，需再次运行
```
![image](https://zmlwzx.github.io/images/VMware/3.png)

4. 创建虚拟机名称

![image](https://zmlwzx.github.io/images/VMware/4.png)

5. 此处都是默认安装

![image](https://zmlwzx.github.io/images/VMware/5.png)

6. “自定义硬件”可根据自己的需求进行配置，本人没有配置

![image](https://zmlwzx.github.io/images/VMware/6.png)
---

## Mac 系统配置
---
- 此时发现有如下报错，需要修改Mac-10.vmx(虚拟机名称)文件，编辑VMX文件，在 smc.present = "TRUE" 后面添加了 smc.version = 0,保存退出,重新启动客户机。

![image](https://zmlwzx.github.io/images/VMware/7.png)
![image](https://zmlwzx.github.io/images/VMware/8.png)

- 安装Mac OS
1. 进入安装界面

![image](https://zmlwzx.github.io/images/VMware/10.png)

2. 选择简体中文，点击下一步箭头

![image](https://zmlwzx.github.io/images/VMware/11.png)

3. 一直点击继续或下一步即可

![image](https://zmlwzx.github.io/images/VMware/12.png)
![image](https://zmlwzx.github.io/images/VMware/13.png)

4. 点击同意

![image](https://zmlwzx.github.io/images/VMware/14.png)

5. 点击界面上方实用工具----->磁盘工具

![image](https://zmlwzx.github.io/images/VMware/15.png)

6. 选择VMware Virtual SATA Hard Drive Media，点击界面上方抹去，设置名称Mac OS，点击 抹去

![image](https://zmlwzx.github.io/images/VMware/16.png)

7. 点击完成，并退出磁盘工具。

![image](https://zmlwzx.github.io/images/VMware/17.png)

8. 选择mac OS，点击继续

![image](https://zmlwzx.github.io/images/VMware/18.png)

9. 等待安装完成

![image](https://zmlwzx.github.io/images/VMware/19.png)

10. 选择中国，点击继续

![image](https://zmlwzx.github.io/images/VMware/20.png)

11. 一直点击继续，需要是否同意 点击 同意

![image](https://zmlwzx.github.io/images/VMware/21.png)
![image](https://zmlwzx.github.io/images/VMware/22.png)

12. 可以点击稍后设置,设置全名和密码，点击继续

![image](https://zmlwzx.github.io/images/VMware/23.png)
![image](https://zmlwzx.github.io/images/VMware/24.png)
![image](https://zmlwzx.github.io/images/VMware/25.png)

13.完成安装
![image](https://zmlwzx.github.io/images/VMware/26.png)

14. 安装后可看到以下的界面，右面有个盘符提示，可以选择推出，这个是苹果的安装系统！
至此，高大上的黑苹果安装完毕！但此处会发现虚拟机中的屏幕无法全屏，这时候需要安装下Vmware Tools，才能全屏。

## 安装下Vmware Tools
1. 在安装Vmware Tools前，保证先右键点击桌面右上角的DVD图标，选择【推出"Sierra Custom Installer"】，如果不推出，此时报错“无法继续执行此操作，因为Mac OS客户机正在使用CD/DVD”。点击VMware的菜单【虚拟机】->【安装 VMware Tools】。

![image](https://zmlwzx.github.io/images/VMware/27.png)
![image](https://zmlwzx.github.io/images/VMware/28.png)

2. 双击打开桌面右上角的【VMware Tools】
3. 在弹出窗口中双击【安装 VMware Tools】
4. 在下一个层叠弹出窗口中点击【继续】->【继续】
5. 在下一个弹出窗口中点击【安装】->【继续安装】
6. 输入Mac OS系统的登录密码，点击【安装软件】
7. 安装成功后，点击【重新启动】

![image](https://zmlwzx.github.io/images/VMware/29png)

8. 联网
```
注意：如果此时Mc OS连接不上网络，是因为VMware的服务还处于关闭状态，全部开启即可。
VMWare 安装完成后，打开任务管理器：win+R，输入 services.msc，将关于 VMware 的服务全部启动运行 
```
---



