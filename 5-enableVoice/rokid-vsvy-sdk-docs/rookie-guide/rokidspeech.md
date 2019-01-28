## 目录

本文介绍如何通过“Rokid开放平台”如何接入我们的语音能力。

![](images/1.jpg)

* [一、创建和配置产品](#一、创建和配置产品)
  * [登录平台账号](#1.登录平台账号)
  * [创建产品](#2.创建产品)
  * [配置产品](#3.配置产品)
  [二、技能配置](#https://developer.rokid.com/docs/5-enableVoice/rokid-vsvy-sdk-docs/rookie-guide/skillstore.html)
* [三、对接 Rokid 语音能力](#三、对接Rokid语音能力)
  * [SDK下载](#1、SDK下载)
  * [开放平台接口定义](#https://developer.rokid.com/docs/3-ApiReference/openvoice-api.html)

  
### 一、创建和配置产品

#### 1.登录平台账号

**若没有账号请先注册，再登录**

使用Rokid开放平台的语音整体方案，请先点击“[Rokid开放平台](https://developer.rokid.com/#/)”首页右上方的【登录】按钮，登录“Rokid开放平台”。如果未有账号，则点击旁边的【注册】按钮进行注册。如下图所示。

![](images/01.png)

登录后，进入“Rokid开放平台”的控制台。首先阅读《开发者社区服务协议》，同意该协议则勾选【同意并接受该协议所有内容】，点击【确定】。如下图所示。
![](images/fuwuxieyi.jpg)

在【语音整体方案】板块，点击【立即接入】，即可开始使用语音接入工具。如下图所示。

![](images/02.png)


#### 2.创建产品

产品是指您想要接入Rokid语音服务的一种实体设备，一个产品只对应一种语音配置。如您想要实现多种语音配置效果，需要创建多个产品。

注册完成后，在“[**Rokid开放平台官网**](https://developer.rokid.com/#/)”点击【语音接入】后，就可以进入创建产品的页面。

- 首次创建产品，可以查看到【创建流程】，点击【一键接入】即可进行创建产品。 如下图所示。
  ![](images/03.png)

- 若账号下已有创建过的产品，若想直接编辑已有产品，点击图标为笔的按钮；若想创建新的产品，点击页面右上角的【一键接入】即可。如下图所示。

  ![](images/04.png)


##### 填写产品基本信息

填写产品相关的【方案类型】、【系统类型】、【产品名称】、【产品描述】、【产品图片】等基本信息。

**注意：**【方案类型】分为 [**全链路通用方案**](./fullLink/fulllink.md) 和 [**基础语音模块**](./speechTTS/speechtts.md) 两种。两者的主要区别是：全链路方案会包含前端模块（拾音方式和MIC阵列），基础语音模块不包含前端模块（拾音方式和MIC阵列）。

![](images/05.png)



#### 3.配置产品

#### 语音配置

#### **1)前端语音配置**

可根据硬件产品选择【拾音方式】、【麦克风阵列】，并设置【激活词】。如下图所示。

##### 激活词

**`激活词`**即**`唤醒词`**，默认为“若琪”，该激活词已经进行训练，唤醒率比较高，测试时为了保障效果建议使用“若琪”。

设置自定义激活词，请单击**`激活词`**输入框输入想要的激活词；**`激活词`**支持4～5个汉字，不建议使用拼音相同的叠字或带有“若琪”字眼的词语，**`激活词`**的评分需在3星以上才能保存。

若您选择了自定义**`激活词`**，且要求优秀的唤醒效果，建议联系商务（商务邮箱：rokidopen@rokid.com）申请数据训练。

![](images/123.png)


#### **2)语音合成配置**

当前页面下拉，编辑“语速”、“发音音域”等可自定义配置语音合成效果。目前只支持【若琪声音-普通话】的调用。其他类型合成音只提供在线试听，暂不可应用到设备，后期会实现应用至设备端。 

![](images/456.png)

##### 服务工具配置

服务工具的配置，包括热词和拦截器配置。热词主要为了提升识别率；拦截器主要适用于兜底聊天和技能家居服务。 具体参照以下指南：

[热词管理接入指南](https://developer.rokid.com/docs/5-enableVoice/rokid-vsvy-sdk-docs/important-concept.html)

[拦截器设置接入指南](https://developer.rokid.com/docs/3-ApiReference/rokid-interceptor.html)

![](images/125.png)

### 二、技能配置

技能配置详见[技能开通文档]（https://developer.rokid.com/docs/5-enableVoice/rokid-vsvy-sdk-docs/rookie-guide/skillstore.html）

### 三、对接Rokid语音能力

1、SDK下载

完成产品的创建和配置后，即可获取产品的SDK。获取SDK有如下两种方式。

#### 方式一

在【产品列表】页面下，选择相应的产品选项卡，点击选项卡右下角的下载图标，即可下载产品SDK。如下图所示。
![](images/127.png)

#### 方式二

在产品的编辑页面，点击页面左上角【SDK下载】即可获取产品的SDK。

![](images/sdk.jpg)

点击后会弹出如下页面，可选择下载SDK、获取测试序列号或在线测试产品等。如下图所示。还可以看到设备的TypeID、key和Secret

![](images/sdk04.png)

2、按照[开放平台接口定义文档](https://developer.rokid.com/docs/3-ApiReference/openvoice-api.html) 进行开发。
