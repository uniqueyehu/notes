# 写在前面的话
使用xxnet的话，不要使用国产杀毒、管家以及浏览器等软件！包括但不限于xxx毒霸、xxx管家、xxx安全卫士（咳咳，不想[被请喝茶](https://github.com/XX-net/XX-Net/issues/5983)的话:smile:），废话不多说，开始配置。

# 安装和配置
## 安装浏览器插件
首先你需要一个Chrome浏览器，并安装扩展应用SwitchOmega，这是用来切换代理的一个插件。如果无法访问Chrome商店的话，可以在下载xxnet后，使用 `XX-Net\SwitchyOmega\SwitchyOmega.crx` 拖放到浏览器扩展程序页面来离线安装。

## 获取和运行xxnet
可以去GitHub上获取[xxnet](https://github.com/XX-net/XX-Net)，选择稳定版下载。下载完成后解压，可以发现有三个启动脚本，windows上使用 `start.bat` 和 `start.vbs` ，Linux和Mac上使用 `start` 来启动xxnet。

![xxnet-start](https://raw.githubusercontent.com/uniqueyehu/uniqueyehu.github.io/master/images/xxnet-start.png)

## 导入bak文件
安装好SwitchOmega了以后，在安装扩展程序的页面找到SwitchOmega，点击 `选项` 。在设置界面点击左边的 `导入导出` 选项，选择 `从备份文件恢复` ，将xxnet目录下 `XX-Net\SwitchyOmega\OmegaOptions.bak` 文件导入进去。

![xxnet-bak](https://raw.githubusercontent.com/uniqueyehu/uniqueyehu.github.io/master/images/xxnet-bak.png)

## 部署appid
### 使用公共appid
在没有自己的appid之前，可以使用公共的appid来配置，打开xxnet的设置页面：[http://127.0.0.1:8085](http://127.0.0.1:8085)，切换到GAEPROXY的 `配置` 选项，点击 `保存` 按钮即可。若要使用自己的appid来部署，需要先创建自己的appid。

### 创建自己的appid
我们需要使用[GoogleCloudPlatform](https://console.cloud.google.com/start)来新建appid的项目，使用得到的项目id来部署xxnet。具体可参照[how to create my appids](https://github.com/XX-net/XX-Net/wiki/how-to-create-my-appids)，写得已经很详细了。

![appid](https://raw.githubusercontent.com/uniqueyehu/uniqueyehu.github.io/master/images/appid.png)

### 部署自己的appid
获取到appid后，打开xxnet的设置页面：[http://127.0.0.1:8085](http://127.0.0.1:8085)，切换到GAEPROXY的`部署服务端`选项，输入自己的appid后，点击`开始部署`按钮，稍后会弹出Google的授权窗口，点击`Allow`，接着会进行服务端的部署。

![xxnet-server](https://raw.githubusercontent.com/uniqueyehu/uniqueyehu.github.io/master/images/xxnet-server.png)

部署完成后，切换到`配置`选项，输入部署好的appid后，点击`保存`按钮，切换到`状态`选项来确认状态。

![xxnet-stat](https://raw.githubusercontent.com/uniqueyehu/uniqueyehu.github.io/master/images/xxnet-stat.png)

### 新世界的大门已经打开
在Chrome浏览器的工具栏中找到SwitchyOmega（一个圆环的图标），点击下面的 `系统代理` 或者 `自动切换` ，对应于xxnet的 `全局PAC智能代理` 和 `取消全局代理` 来选择适合你的模式:blush:

### 小小的说明
1. 每个AppID每天1G流量，一般每个Google帐户最多12个AppID
2. AppID的数量只影响流量，不影响速度

# 参考
1. [XX-Net中文文档](https://github.com/XX-net/XX-Net/wiki/%E4%B8%AD%E6%96%87%E6%96%87%E6%A1%A3)
2. [安装和使用 SwitchyOmega](https://github.com/XX-net/XX-Net/wiki/%E5%AE%89%E8%A3%85%E5%92%8C%E4%BD%BF%E7%94%A8-SwitchyOmega)