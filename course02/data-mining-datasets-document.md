# 数据挖掘文档
## 数据背景
#### 1、memdical_qa表
数据源来自某在线求医产品的中文医患对话数据（好大夫）haodf.com
原始描述:The MedDialog dataset contains conversations (in Chinese) between doctors and patients. It has 1.1 million dialogues and 4 million utterances. The data is continuously growing and more dialogues will be added. The raw dialogues are from haodf.com. All copyrights of the data belong to haodf.com.

#### 2、doctor_msg表
数据源来自某在线求医产品的中文医患对话数据（好大夫）haodf.com
1、首先获取好大夫网站注册医生的信息中心页，获取【医生姓名,医院科室,信息中心页】
2、再通过以上数据获取医生个人网站和评价分享链接【医生姓名,医生ID,个人网站,评价分享链接】
3、最后通过以上数据获取医生在线咨询服务的详细信息【医生姓名,医生ID,医院科室,医生职称,患者投票数,疗效满意度,态度满意度,图文线上门诊价格,图文一问一答价格,电话咨询价格,24小时回复率,24小时接听率,电话咨询综合评分】
## 数据格式
**已脱敏**
![f81fccb0929ee26a6bfcbdd2216f1d7a.png](en-resource://database/1432:1)

### 字段说明
#### memdical_qa表
>医生&患者问答数据表


id：id唯一标识
department：所属科室
title：Q&A标题
ask：患者问题
answer：医生回答

#### doctor_msg表
>医生个人信息表

id：id唯一标识
doctor_name：医生姓名
doctor_id：医生id
doctor_department：医生科室
doctor_title：医生职称
patient_vote：患者投票数
treatment_satisfaction：疗效满意度
attitude_satisfaction：态度满意度
online_outpatient_price：线上门诊价格
online_qa_price：线上一问一答价格
response_rate：24小时回复率
reception_rate：24小时接听率
telephone_price：电话咨询价格
telephone_score：电话咨询综合评分

## 数据应用方案

- 医疗自动问答
- 患者自动匹配热门医生
- 等等


## 参考
- https://github.com/yijieshi/haodf-offline-crawler-scripts
- https://github.com/Toyhom/Chinese-medical-dialogue-data