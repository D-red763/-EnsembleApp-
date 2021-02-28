# -EnsembleApp-

异构系统和异构消息的集成方案

概述：
随着现代医院建设的信息化程度越来越高，对接的子系统数量也越来越多，系统的架构、接口类型、消息结构越来越复杂，对医院系统之间的信息传递造成很大不便。为了解决该问题，我们采用HL7、XML等标准，使用Ensemble内置的数据转换工具（DT），将异构系统的接口进行标准化（通常引用Soap、REST、TCP/IP等标准协议），使得不同架构的系统，即时接口类型不同、消息模型不同，也能进行数据的传输。
关键词：HL7、XML、Settings、DataTransform、JDBC、SQL

应用程序内容：
采用的数据结构（Doctype）有：HL7、XML，在BS采用JDBC连接数据库、配置SQL获取数据源，并通过Settings对消息的传输目标进行配置化管理。

应用链接：
https://github.com/D-red763/-EnsembleApp-/blob/main/Application/BS/ScanForADT.xml


HL7 Schema与XML Schema
HL7为Ensemble内置的一种消息结构，通常被应用在医疗行业的数据传输方面。
XML是一种用于标记电子文件使其具有结构性的标记语言，在各个行业的数据传输方面被广泛应用，Ensemble当然提供了解析工具。

应用链接：
https://github.com/D-red763/-EnsembleApp-/blob/main/Application/MSG/PhyApplyRequest.xml
https://github.com/D-red763/-EnsembleApp-/blob/main/Application/MSG/HL7Schema.png


DataTransform
是Ensemble内置的消息DocType转换器，并提供了图形化的管理界面。使用此工具，我们可以对XML和HL7不同结构的消息进行相互转换。

应用链接：
https://github.com/D-red763/-EnsembleApp-/blob/main/Application/Translate/ADTC2HL7.xml


应用样例：
本应用程序只展示患者信息的数据集成，通过查询数据库中的患者数据集，组装成标准的XML消息后，转换成HL7格式，转发给不同的系统（BO），这些目标系统采用的接口协议有Soap、HTTP、TCP/IP，都可以通过Esnemble内置Adapter进行开发。

Production配置：应用程序截图说明/ProductionConfig.png

BS配置：应用程序截图说明/BS_Config.png ; 应用程序截图说明/BS_Setting_Config.png ;

Transform配置过程：应用程序截图说明/Transformation.png

Router中应用Transform：应用程序截图说明/Rules_Translate.png

BO可直接引用Ensemble的内置Operation类进行开发：
https://github.com/D-red763/-EnsembleApp-/blob/main/Application/BO/BO-HTTP%E9%85%8D%E7%BD%AE.png
https://github.com/D-red763/-EnsembleApp-/blob/main/Application/BO/BO-Soap%E9%85%8D%E7%BD%AE.png
https://github.com/D-red763/-EnsembleApp-/blob/main/Application/BO/BO-TCP%E9%85%8D%E7%BD%AE.png


English Description

Integration scheme for heterogeneous messages in heterogeneous systems

Summary:
With the increasing information level of modern hospital construction, the number of docking subsystems is also increasing, and the system architecture, interface type and message structure are becoming more and more complex, which causes great inconvenience to the information transmission between hospital systems.In order to solve the problem, we use the standard such as HL7, XML, use the Ensemble's built-in data conversion tool (DT), the heterogeneous system to standardize the interfaces (typically reference standards such as Soap, REST, TCP/IP protocol), makes the different architecture of the system, real-time interface types, message model is different, also can for data transmission.

Keywords: HL7, XML, Settings, Datatransform, JDBC, SQL

Application Content:
The data structures (DOCTYPE) adopted include HL7 and XML. In BS, JDBC is used to connect to the database, SQL is configured to obtain the data source, and the transmission target of the message is configured and managed through Settings.

Application link:
https://github.com/D-red763/-EnsembleApp-/blob/main/Application/BS/ScanForADT.xml

HL7 Schema and XML Schema
HL7 is a message structure built into Ensemble that is commonly used for data transmission in the healthcare industry.
XML, a markup language for structuring electronic documents, is widely used for data transfer in a variety of industries, and Ensemble certainly provides the parsing tools.
Application link:
https://github.com/D-red763/-EnsembleApp-/blob/main/Application/MSG/PhyApplyRequest.xml
https://github.com/D-red763/-EnsembleApp-/blob/main/Application/MSG/HL7Schema.png

DataTransform
Ensemble is a built-in message DOCTYPE converter, and provides a graphical management interface.Using this tool, we can convert XML and HL7 messages with different structures to each other.
Application link:
https://github.com/D-red763/-EnsembleApp-/blob/main/Application/Translate/ADTC2HL7.xml

Example:
This application only demonstrates the data integration of patient information by querying patient data sets in the database, assembling them into standard XML messages, converting them into HL7 format, and forwarding them to different systems (BOs) using interfaces such as SOAP, HTTP, and TCP/IP, all of which can be developed using the built-in Adapter for eSnemble.

Production configuration: application screenshot description/productionconfig.png

BS configuration: application screenshot description/bs_config.png;/ bs_setting_config.png; / bs_setting_config.png;

Transform configuration process: Application screenshot description/transformation.png

Router-Transform: Application Screenshot/rules_translate.png

BO can be developed directly by referring to Ensemble's built-in Operation class:
https://github.com/D-red763/-EnsembleApp-/blob/main/Application/BO/BO-HTTP%E9%85%8D%E7%BD%AE.png
https://github.com/D-red763/-EnsembleApp-/blob/main/Application/BO/BO-Soap%E9%85%8D%E7%BD%AE.png
https://github.com/D-red763/-EnsembleApp-/blob/main/Application/BO/BO-TCP%E9%85%8D%E7%BD%AE.png
