# MongoDB 跨数据中心部署

MongoDB白皮书，2017年11月

参考

https://www.jianshu.com/p/b11e14e68abc

- [MongoDB 跨数据中心部署](#mongodb-跨数据中心部署)
  - [介绍](#介绍)
  - [维护服务的延续性](#维护服务的延续性)
    - [副本集Replica Sets](#副本集replica-sets)
  - [扩展MongoDB的持续可用性](#扩展mongodb的持续可用性)
  - [MongoDB数据中心识别](#mongodb数据中心识别)
  - [MongoDB部署模式](#mongodb部署模式)
  - [管理跨数据中心部署方案](#管理跨数据中心部署方案)
  - [MongoDB跨数据中心线上部署](#mongodb跨数据中心线上部署)
  - [结论](#结论)
  - [资源](#资源)
  - [关键词](#关键词)

## 介绍

关键业务应用必须保证其服务的持续性。随着越来越多的组织需要为全球用户提供线上服务，确保服务在各个分布的地理区域的可用性和可扩展性，在系统设计中变得越来越重要。

将数据库在多个数据中心的区域分布，有三个重要原因：

- **持续可用性：**无论是在自有机房还是公有云上部署数据库，当某个区域发生火灾、洪水或者飓风等灾难导致数据中心停电或断网时，业务方都需要确保服务能够正常使用。Gartner估计宕机造成的业务损失是平均每小时30万美元，如果是面向全球的互联网服务，损失则会更高。
- **用户体验：**不管用户在哪里，用户都需要一致的、低延迟的体验。Amazon有个著名的结论：每增加100ms延迟，导致销售额损失1%。
- **数据合规：**各个国家政府都会控制客户数据存储的地点，数据是不允许被存储在国界之外的。

通过数据中心识别的复制、自动伸缩以及自动化运维，MongoDB可以在全球范围内高效地部署应用，帮助组织用极低的成本、快速开拓市场、达成很高的用户满意度。用户可以自由选择将MongoDB服务部署在自建的数据中心、或者公有云提供商提供的数据中心，又或者直接使用跨区复制的MongDB Atlas云数据库服务。

本白皮书探索了MongoDB数据中心识别的技术基础，展示了多个部署场景，并用线上用户的示例做出总结。

## 维护服务的延续性

在日常运维条件下，MongoDB都能实现系统的性能和功能目标。但是，时而不时总有不可避免的失败或者操作失误导致系统无法正常运行。存储设备、网络链接、电力供应以及其他硬件设备总会出现故障，通过备份可以减少这类风险。类似的，MongoDB数据库支持软件组件以及数据存储等的冗余配置。

### 副本集Replica Sets

MongoDB原生的复制功能维护多个数据副本，叫作副本集。用户应该部署副本集来避免数据集宕机。副本集可以自我恢复，因为Failover和恢复全程都是自动的，当发生故障时不需要人为的介入来恢复系统。

通过副本集还可以更灵活地维护系统（例如硬件升级、软件升级），

## 扩展MongoDB的持续可用性

## MongoDB数据中心识别

## MongoDB部署模式

## 管理跨数据中心部署方案

## MongoDB跨数据中心线上部署

## 结论

## 资源

## 关键词

- **Regulatory Compliance：**合规
- **on-premise：** [解释](private-cloud&on-premise.md)
- **outage：**停电或者网络中断，a period when a power supply or other service is not available or when equipment is closed down
- **adverse：**preventing success or development; harmful; unfavorable
- **mitigate：**make less severe, serious, or painful缓和、减轻
- **intervene：**come between so as to prevent or alter a result or course of events，介入，阻挠