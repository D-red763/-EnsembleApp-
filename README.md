# -EnsembleApp-

异构系统和异构消息的集成方案
Integration scheme for heterogeneous messages in heterogeneous systems

概述：
随着现代医院建设的信息化程度越来越高，对接的子系统数量也越来越多，系统的架构、接口类型、消息结构越来越复杂，对医院系统之间的信息传递造成很大不便。为了解决该问题，我们采用HL7、XML等标准，使用Ensemble内置的数据转换工具（DT），将异构系统的接口进行标准化（通常引用Soap、REST、TCP/IP等标准协议），使得不同架构的系统，即时接口类型不同、消息模型不同，也能进行数据的传输。
关键词：HL7、XML、Settings、DataTransform、JDBC、SQL

应用程序内容：
采用的数据结构（Doctype）有：HL7、XML，在BS采用JDBC连接数据库、配置SQL获取数据源，并通过Settings对消息的传输目标进行配置化管理，

HL7 Schema与XML Schema
HL7为Ensemble内置的一种消息结构，通常被应用在医疗行业的数据传输方面。
XML是一种用于标记电子文件使其具有结构性的标记语言，在各个行业的数据传输方面被广泛应用，Ensemble当然提供了解析工具。

应用链接：
https://github.com/D-red763/-EnsembleApp-/blob/main/Application/MSG/PhyApplyRequest.xml


