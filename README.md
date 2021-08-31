# 中文简体 | [English](https://github.com/DHDAXCW/NanoPi-R4S-2021/blob/main/EngLish.md)
# NanoPi-R4S-2021 每天自动更新插件和内核版本。
## 👉使用本固件前，请严格遵守国家互联网使用相关法律规定,不要违反国家法律规定！👈
## 强烈推荐三星TF卡\海康TF卡。哪怕是很难刷上的固件，只有三星刷上可以开机。
### 固件分类 在[releases](https://github.com/DHDAXCW/NanoPi-R4S-2021/releases)有备注关键词
- 正式版（含超频）对折腾的，可以选择，电压一定要考虑。超频都是升压的，会造成不稳定的。比如跑cpu测试容易升压等。
- Docker版 含Docker插件，会导致udp转发失效 慎用哦，只要别开passwall的udp，啥都不影响使用！
- 默频版 移除超频补丁，改为官方默认频率，合适不折腾的所需。电压多少都无所谓，它稳定贼好！（推荐）格式建议刷sq格式 合适小白。如果需要挂载，选择ext4
- 精简版 我不说了哈  就保留了helloworld passwall ssrp uu加速器等。。。
### 注：不要用恢复备份。。不保证某个插件是否正常运行。。。建议重新设置贼好！！！
这一个月我没电脑都在讨乞（求电脑中~）。。。需要一个WiFi模块，工业级WiFi模块MiniPCIe高通QCA9984芯片compex wle1216vx 在x86上做测试。淘宝商铺都没有货了。谁有此模块，请加入电报群找💀谢谢
### 默认编译  

- 用户名：root 密码：password  管理IP：192.168.2.1
- 下载地址： https://github.com/DHDAXCW/NanoPi-R4S-2021/releases
- x86_64固件下载 https://github.com/DHDAXCW/lede/releases
### - Docker：正式版带docker，有超频，带有docker插件。（对passwall的udp要求很高，不要刷docker版本）
### - Overclocking：默认版，无超频
### - formal edition：正式版，有超频
- 精简版 ：https://github.com/DHDAXCW/NanoPi-R2S-R4S-2021-mini/releases
- 电报群：https://t.me/DHDAXCW
- X86固件 ：[点击链接下载](https://github.com/DHDAXCW/lede/releases)
# 在线升级
- 复制以下代码，在TTYD终端执行，过程中不得离开，否则还得重新下载，请刷ext4格式明天再升级
### 该升级只支持4G版，1G版不支持，请不要用此升级。1G版内存tmp分区空间不足，无法下载升级包
- 多版本在里面，自己选 👇
```
wget https://raw.githubusercontent.com/DHDAXCW/NanoPi-R4S-2021/main/scripts/autoupdate.sh && sh autoupdate.sh
```
# 赏个鸡腿吧
 ![Alt text](data/2.jpg?raw=true "Title")
### 如果你觉得此项目对你有帮助，可以捐助我们，以鼓励项目能持续发展，更加完善
# 插件展示
 ![Alt text](data/20.jpg?raw=true "Title")
## 提示
 - 我的固件加了动态超频，不管热不热这是取决后台运行程序在跑什么。
 - 感觉很热  就加风扇，推荐 风扇6cm×6cm，薄1cm，usb也行 或者端子线zh1.5

### 更新日志 9.1
- 优化部分应用插件

### 更新日志 8.12
- 新增cpu控制器，方便调整频率
- 针对r4s超频补丁进行优化
- 更改内核对低速TF卡的优化支持
- 修复passwall全协议缺失问题等
- 修复passwall在Simple-Obfs的编译问题。
- 再次优化r4s在低速TF卡，防止启动DOCKER写入导致崩  我建议最好换高速卡。。。比如三星，海康等
- 优化多拨在低速卡情况下写入缓存导致灯全亮 还是建议换最牛B高速卡解愁。。
- 移除bypass，会导致杀死smartdns
- 其他编译流程修复和优化。
