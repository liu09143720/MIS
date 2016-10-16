# MIS
##ER图
![ER图](https://github.com/liu09143720/MIS/blob/master/ER%E5%9B%BE.png)
##数据库


22:34:03
~陈旭翔 2016/10/16 22:34:03
DROP TABLE IF EXISTS 保养信息;
/!40101 SET @saved_cs_client = @@character_set_client */;
/!40101 SET character_set_client = utf8 /;
CREATE TABLE 保养信息 (
保养ID int(11) NOT NULL,
F保养类别 varchar(255) CHARACTER SET big5 NOT NULL,
保养人 varchar(255) NOT NULL,
PRIMARY KEY (保养ID)
DROP TABLE IF EXISTS 保养记录;
/!40101 SET @saved_cs_client = @@character_set_client /;
/!40101 SET character_set_client = utf8 /;
CREATE TABLE 保养记录 (
记录Id int(11) NOT NULL,
F设备ID int(11) NOT NULL,
F保养ID int(11) NOT NULL,
保养时间 date NOT NULL,
说明 varchar(255) NOT NULL,
PRIMARY KEY (F保养ID)DROP TABLE IF EXISTS 检修情况;
/!40101 SET @saved_cs_client = @@character_set_client /;
/!40101 SET character_set_client = utf8 /;
CREATE TABLE 检修情况 (
Id int(11) NOT NULL,
保养内容 varchar(255) NOT NULL,
完成状况 varchar(255) NOT NULL,
备注 varchar(255) DEFAULT NULL,
FF设备ID varchar(45) NOT NULL,
PRIMARY KEY (FF设备ID)DROP TABLE IF EXISTS 检修项目;
/!40101 SET @saved_cs_client = @@character_set_client /;
/!40101 SET character_set_client = utf8 /;
CREATE TABLE 检修项目 (
设备类别 varchar(255) NOT NULL,
保养类别 varchar(255) NOT NULL,
保养内容 varchar(255) NOT NULL,
PRIMARY KEY (设备类别)DROP TABLE IF EXISTS 消耗记录;
/!40101 SET @saved_cs_client = @@character_set_client /;
/!40101 SET character_set_client = utf8 /;
CREATE TABLE 消耗记录 (
消耗ID int(11) NOT NULL,
修理内容 varchar(255) NOT NULL,
消耗材料 varchar(255) NOT NULL,
消耗数量 int(11) DEFAULT NULL,
剩余数量 int(11) NOT NULL,
消耗记录col varchar(45) NOT NULL,
PRIMARY KEY (消耗ID)DROP TABLE IF EXISTS 设备信息;
/!40101 SET @saved_cs_client = @@character_set_client /;
/!40101 SET character_set_client = utf8 */;
CREATE TABLE 设备信息 (
设备ID int(11) NOT NULL,
F设备类别 varchar(255) NOT NULL,
最近一次保养时间 date DEFAULT NULL,
PRIMARY KEY (F设备类别)
