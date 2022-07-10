
## 简历

---

### 个人信息
```
王福顺
电话,微信: 13096394283 
邮箱: shi_qinghai@outlook.com
年龄: 26岁
性别: 男 
工作经验: 3年
```

### 求职方向

 - 城市: 成都 
 - 岗位方向: 大数据开发,实时数仓开发


### 专业技能
 - 编程语言: java,scala,shell脚本
 - 计算框架: hadoop系列,spark,flink
 - mpp数据库: clickhouse,doris
 - 其他: 各种工具类软件安装运维使用,如 cacel,dbz,kafka,zk,flink等等
  
### 工作经历
 - 深圳沸石科技股份有限公司  
    - 2019年7月~2020年4月
    - 基于nifi进行数据接入开发,数据库维护等


  - 东方国信科技股份有限公司
    - 2020年6月~2021年5月
    - 负责spark开发,基于hive的etl脚本开发


  - 成都我行我数科技有限公司
    - 2021年9月~至今
    - 基于flink的实时业务开发,基于hive数仓的etl作业开发.基于flink sql的实时数仓设计开发

### 项目经历
 - 私有化看板
    - 简介: 以doris作为数据库,azkaban作为调度工具,数据源采用flink cdc从mysql获取.将一些数仓指标任务进行私有化部署.
    - 工作内容: 整体方案设计,全流程软件安装部署,程序样例开发.并参与部分业务sql开发.
    - 技术栈: flink,azkaban,doris,shell
  

 - 实时标签开发
    - 简介: 从mysql拉取数据整理分类后,并转化为flink sql能识别为change流的格式写入kafka,按照数仓分层设计将数据在kafka分层,最后从数据集实时计算出各个标签值写入es.全流程用flink sql实现,达到实时的效果.
    - 工作内容: 整体方案设计,全流程软件安装部署,程序样例开发.并参与部分业务开发.
    - 技术栈: flink cdc,kafka,flink sql
  

 - 实时one id改造
    - 简介: 传统oneid算法,是使用spark图计算来进行批量计算.每次计算需要全量数据作为基本条件,随着数据量增加,每次计算耗时增加,当前单次任务耗时约3小时.实时标签需要实时关联oneid来作为最后的数据依赖,因此需要oneid能实时得到.最后设计了以实时计算的思想来实现图计算中计算最大连通图的效果,并通过flink来实现.单次任务耗时与新增数据量相关,目前一般任务耗时减少为3分钟左右.同时为了兼容旧有的hive数仓作业,完成了以shell提交flink sql批任务,并返回结果给shell的分支程序.
    - 工作内容: 技术改造设计,开发测试.
    - 技术栈: flink,redis,hbase,shell,yarn


  - 实时数仓数据抽取改造 
    - 简介: 一般情况,根据业务需求,自己新建作业使用flink cdc抽取mysql源数据.但是随着作业增加,各个任务将会出现重复抽取,抽取链接过多的问题.为此需要进行统一分层设计.根据我们的业务需求,最后实现固定的若干flink cdc程序来进行源数据抽取,并解析为dbz json的格式发送到kafka.后续其他业务需要数据,从kafka过滤获取即可.同时,在整体抽取的程序中,插入我们抽取oneid源数据的流程,并通过redis 订阅/发布的功能完成配置初始化及配置实时更新的功能.
    - 工作内容: 设计开发
    - 技术栈: flink cdc,kafka,redis


  - flink开发工具搭建
    - 简介: 为了使刚接触flink的工程师快速上手开发,同时整合一些标准开发任务,并且实现flink sql快速开发,做了如下工作:
      - flink快速开发骨架: 这是一个maven骨架,在官方骨架的基础上,实现了开发测试环境切换,涵盖了es,kafka,hbase,clickhouse等常用connector包装及示例.
      - flink作业模板开发: 将一些标准作业开发为模板,通过修改配置文件即可启动不同的任务.如: kafka写入hive模板,mysql同步到clickhouse模板,mysql同步到doris模板等.
      - dlink安装演示: 这是一个web端的flink sql客户端,类似于一个flink sql ide,可以快速开发sql任务并提交到指定集群中.调研相关软件之后选择了dlink,并在测试环境中搭建并进行相关样例程序开发.


  - 独立flink任务开发
    - 简介: 除了数仓相关的任务,还有一些数仓外来自于我们sass产品的实时开发需求.这些需求一般不进行数仓类的分层,各个作业单独设计实现.技术上包含了flink大部分特性.
    - 工作内容: 开发测试
    - 技术栈: flink,redis,es,clickhouse,kafka
  
### 开源项目
  - flink-quickstart
    - maven骨架,在官方骨架的基础上,将常用的flink connector进一步用建造者模式包装并完善注释,能更方便的快速开发


  - flink-connector-lettuce-redis 
    - 用于flink sql的redis connector实现,相比其他开源实现,区别如下:
      - 底层使用的是lettuce,多线程安全的redis客户端
      - 兼容支持flink中的标准格式:csv,json
      - lookup功能使用异步实现,sink功能使用同步实现

### 其他

 - 在线简历: https://dahai1996.github.io/sqh.gihub.io/
 - github: https://github.com/dahai1996

