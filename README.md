# API_museum 智能博物馆设计

Title|Content
-----|:------
发布日期|2019-12-16
名称|智能博物馆APP
文档状态|进行中
文件主人|	谢颖
领头的设计师|	谢颖
领头的开发者|	谢颖
领头的测试者|	谢颖


### 价值主张练习
- **一句话版本**
我们致力于为博物馆提供更方便快捷的游客管理系统，协助博物馆的工作人员对人流量及用户可能发生的危险行为进行系统管理和提高用户观览体验。

- **一份钟版本**
本智能博物馆产品着眼于优化博物馆游客管理系统，旨在令不同的特殊人群（多动症患者）也能享受、观赏到博物馆的展览及领会到其意义。我们计划通过人流量统计API、人脸识别API、危险行为识别api、物体和场景识别API及推荐算法机制对博物馆的导览和监控系统进行优化。我们主要设计三个功能：一是人流量统计功能，通过监测识别人脸统计当前场馆内的游览人数，当超过一定限度人数后，该功能将提示并给出游客前往其他场馆的路线：二，是行为监控功能，此功能将与博物馆内的监控进行结合，对于行为比较偏激或作出危险行为动作的用户发出提示，工作人员也能实时对其行为进行预警和防范；三，是展品的扫描介绍解说功能，用户可通过扫描拍摄或上传相关的展品相片，播放该展览物和场景的相关解说视频，使用户更加集中观览。



## 产品介绍
该智能博物馆app旨在令不同的特殊人群也能享受、观赏到博物馆的展览及领会到其意义。然而大型博物馆存在的结构复杂、客流量大、门票进出需要登记等问题。因此, 博物馆可以通过增加一些技术性设备，以AI人工智能技术加持。基于现状，我们计划通过人流量统计API、人脸识别API、危险行为识别api、物体和场景识别API及推荐算法机制对博物馆的导览和监控系统进行优化。

## 背景
大型博物馆存在的结构复杂、客流量大、门票进出需要登记等问题。对于一些特殊的多动症人群和用户在观览展品时可能会存在注意力不集中和行为无法得到控制的问题，而博物馆专门加设相关人员管理成本就会很高。这款APP对游客或博物馆来说，都是一个很好的选择。

### PRD 价值主张设计 
#### PRD1.加值宣言 
该智能博物馆app旨在令不同的特殊人群也能享受、观赏到博物馆的展览及领会到其意义。然而大型博物馆存在的结构复杂、客流量大、门票进出需要登记等问题。因此, 博物馆可以通过借助一些技术性设备，以AI人工智能技术加持。基于现状，我们计划通过运用百度ai中的人流量统计API、人脸识别API、危险行为识别api及通用物体和场景识别api对博物馆的导览和监控系统进行优化。
优先级：
- 基于区域人流量统计技术模型，运用百度AI中的人流量统计功能，为场馆提供了完善的区域人数统计方案——当区域人数超过限定数值时，系统会自动预警，帮助馆内辅助设施和工作人员及时实行疏散策略，保障潜在的参观者聚集区域长期安全通畅。
- 通用物体和场景识别API,通过拍摄或上传相关展览物品和场景，播放该展览物和场景的相关解说视频，使多动症患者更加集中观览。
次优先：
- 运用人脸识别API，检测用户人脸是否与身份证信息相符，更好地保证博物馆安全问题。
- 危险行为识别API，针对5S内的监控视频片段，识别常见危险行为，对于出现的危险行为及时预警、管控，避免安全事故。

PRD2.核心价值 
#### 核心价值宣言：
1. 人流量统计api:检测博物馆相关场馆内人流量，当人流量较多的场馆给用户提供其他场馆的路线图，提供更好的导览空间，同时也帮助多动症患者规避参观人流量多问题，让患者在有足够空间参观展馆的同时减少与他人发生冲突的危险。
2. 物体和场景识别API：通过拍照识别动作让用户在参观过程中更有交互感，返回的视频介绍信息也比书面信息更能让用户集中注意力。
3. 人脸识别api：可通过app扫描用户人脸，对进入博物馆内的用户进行人脸识别，核实身份信息，发生安全问题时也能通场馆内监控扫描识别，定位到相应的用户上，规避安全隐患。
4. 危险行为识别api：针对5S内的监控视频片段，识别常见危险行为，对于出现的危险行为及时预警、管控，避免安全事故。
#### 人工智能概率性与用户痛点
人工智能能概率性|用户痛点
---------------|:------
可以通过人流量统计和人脸识别更加系统地管理游客流量，让馆内工作人员及时对较拥挤的场馆进行人流量疏通|现在不知道哪个展馆人流量少一点，方便多动症患者活动
监控通过危险行为识别api监测用户是否会发出一些危险行为，馆内工作人可及时管控避免安全事故|多动症患者易与正在观览的用户发生冲突或发生破坏展览物的行为
拍照识别功能可以拍摄照片返回展品视频介绍|多动症患者无法集中注意力观览展品介绍
#### 需求列表与人工智能API加值
用户案例|技术|重要程度
-------|:----:|:----
用户想去一个较少参观者的展馆参观|人流量统计api|非常重要
用户想便捷进入博物馆内|人脸识别api|重要
用户想集中注意力能更快捷了解到展览信息|物体和场景识别api|重要
博物馆需要检测管内有无危险行为发生|危险行为识别api|重要

#### 产品原型
##### 一、交互及界面设计


##### 二、信息设计
- 人流量统计界面
![人流量统计](https://upload-images.jianshu.io/upload_images/9513869-9a647501b24ed8ce.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

- 人脸识别检票界面
![人脸识别](https://upload-images.jianshu.io/upload_images/9513869-f268e46b2e93121e.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)
![生成二维码](https://upload-images.jianshu.io/upload_images/9513869-6f3a50c7354c5dad.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

- 扫描展物获取信息

![扫描展物](https://upload-images.jianshu.io/upload_images/9513869-f326e2d230b2de99.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

![结果](https://upload-images.jianshu.io/upload_images/9513869-fca5533f6a1e1379.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

##### 三、原型文档
- [在线查看原型]()
- [原型下载](https://github.com/Shadowxy22/museum_axure)
