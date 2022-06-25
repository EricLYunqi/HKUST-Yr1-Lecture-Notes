## 写在最前
五十天的寒假接近尾声，于是决定在开学前总结一下寒假学到的知识，以免开学后没了时间。
所谓“工欲善其事，必先利其器”，当机械与硬件的队员终于满怀欣喜地将成品呈现在你的面前，可你还在配置环境，非常难受。而对于Mac特有的尿性，导致网上的博文少之又少，于是博主首先总结一下自己在配置环境中所遇到的困难，以及是如何解决的。
## 正文
博主使用的是19年的MacBook pro，13英寸，Apple M1芯片，macOS Big Sur 11.4。

而博主使用的芯片是 imxrt1052，编译器使用VScode，整体使用RT thread进行代码编写，编写完成后使用Jlink进行烧录调试。

那么首先第一步当然就是在自己的VScode中下载RT thread的扩展
![请添加图片描述](https://img-blog.csdnimg.cn/8e75ff1062f944c488806f422b794cce.png?x-oss-process=image/watermark,type_d3F5LXplbmhlaQ,shadow_50,text_Q1NETiBARXJpY0xZdW5xaQ==,size_13,color_FFFFFF,t_70,g_se,x_16)
下载后得到的这样的结果。（当然其中的工程是博主自己的）。

下载完插件后，还需要下载ARM ToolChain，SEGGER（Jlink），RT Thread Source Code以及自己需要的工程。（其中Jlink我们使用V6.60d）

这里有两个坑，首先下载ARM的时候一定要下载文件名就是“ARM”的文件，第二个是SEGGER文件夹会有两个子目录，其中一个是捷径，我们需要V660d的路径。另外对于JLinkDevices.xml文件也需要相应的添加，这里是根据不同型号确定的。以下是我自己的。

```
<!--                 -->
<!-- NXP (iMXRT105x) -->
<!--                 -->
<Device>
  <ChipInfo Vendor="NXP" Name="MIMXRT1052QSPI" WorkRAMAddr="0x20000000" WorkRAMSize="0x00080000" Core="JLINK_CORE_CORTEX_M7" Aliases="MIMXRT1052xxx5B; MIMXRT1052CVL5B; MIMXRT1052xxx6B; MIMXRT1052DVL6B" />
  <FlashBankInfo Name="QSPI Flash" BaseAddr="0x60000000" MaxSize="0x04000000" Loader="Devices/NXP/iMXRT105x/NXP_iMXRT105x_QSPI.elf" LoaderType="FLASH_ALGO_TYPE_OPEN" />
</Device>
```
另外大部分初学者都需要自己下载已经打包好的工程，这里需要找到source code中的bsp，再找到其中的imxrt，将下载好的工程放在其中即可。

之后在VScode中点击add project to current workspace即可。注意添加的是你下载的工程不是source code

添加好后在VScode终端执行
```
brew install scons
scons --menuconfig
```
即可编译工程（build project）

之后需要对RT thread扩展的设置进行路径配置，需要配置的是 “Adapter”， “GDBpath”，“RTT...flag”，“MDKlocation“，”RTT_ROOT”。

之后如果烧录出现问题就需要更改cortex-debug扩展下workspace的JLink路径文件，具体更改方法因人而异。（需要补加Jlinklocation）

另外提一句，对于Mac来说，如果要新增package的话，需要到自己的env下，就是进入/Usr，同时按下command+shift+句号（。）即可。（显示隐藏的user的环境文件夹）而且一定要注意别忘了改Kconfig，更新完后需要
```
source ~/.env/env.sh
packages --update
```
如果显示失败需要安装requests
```
python -V
cd python
pip install requests
```
即可
如果packages出现问题等等情况，建议多试几次
```
scons --menuconfig
```
toggel一些选项然后保存（等于结果什么都没改）
![请添加图片描述](https://img-blog.csdnimg.cn/d3f893e599fc4008af112322ddeef78a.png?x-oss-process=image/watermark,type_d3F5LXplbmhlaQ,shadow_50,text_Q1NETiBARXJpY0xZdW5xaQ==,size_14,color_FFFFFF,t_70,g_se,x_16)
点击绿色按钮完成烧录。注意每次更改文件后都需要重新保存加编译才可正常烧录。
## 可能出现的问题
~~update at 5/2/2022~~ 

无聊的周末开始回看这篇文奖发现很多地方还是没有说到，比如对于Mac用户来说，不要使用RT thread自带的Debug按钮，因为我们并没有在设置里配置烧录器路径，一定要使用VScode自带的。
以及在烧录中如果报错没有找到GDB路径，那就是当前workspace的Jlink配置文件出了问题，需要在里面添加Jlink的路径，有些人可能还需要删除ARMToolchain的路径。如果报错是超时，一定要注意Jlink有没有连接好，可能没有找到烧录器也会出现原因。

~~正在考虑要不要总结一下Mac配置putty的博文~~ 
