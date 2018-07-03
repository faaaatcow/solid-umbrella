---
title: "data_input_output"
author: "xz"
date: "2018-7-3"
output:
  html_document: default
  pdf_document: default
  word_document: default
---

```{r setup, include=FALSE}
knitr::opts_chunk$set(echo = TRUE)
```

## 1 Data input
数据导入包含多种格式，以下主要说明 **CSV** , **TXT**, **EXCEL**三种:

### CSV
```{r data1}
# 导入
data1 <- read.csv("C:\\Users\\test\\Desktop\\xz\\rstudy\\myfiles.csv")
# 查看前6条记录
head(data1)
```

### TXT
```{r data2}
# 导入
data2 <- read.table("C:\\Users\\test\\Desktop\\xz\\rstudy\\myfileS.txt",header = T)
# 查看前6条记录
head(data2)
```

### EXCEL
安装JAVA JDK, **按系统选择对应版本** <http://www.oracle.com/technetwork/java/javase/downloads/jdk8-downloads-2133151.html>
```{r data3}
##
# 安装工具包
# install.packages("rJava")
# install.packages("xlsx")
# install.packages("xlsxjars")
# 加载工具包
library("rJava")
library("xlsx")
library("xlsxjars")
# 导入
data3 <- read.xlsx("C:\\Users\\test\\Desktop\\xz\\rstudy\\myfiles.xlsx",sheetName = 'Sheet1',header=T,encoding = 'UTF-8')
# 查看前6条记录
head(data3)
```

## 2 data reshape
主要指数据转置，列转行
```{r reshape2}
# 安装工具包
# install.packages('reshape')
# 加载工具包
library('reshape')
# 转置
reshapedata3 <- melt(data3, id.vars = "姓名",variable_name = "科目", value.name = "成绩")
# 查看前6条记录
head(reshapedata3)
```

## 3 data output

### CSV
```{r out_csv}
write.table(reshapedata3, file = "C:\\Users\\test\\Desktop\\xz\\rstudy\\mydata3.csv",
            sep = ',', row.names = FALSE)
```

### TXT
```{r out_txt}
write.table(reshapedata3,file = "C:\\Users\\test\\Desktop\\xz\\rstudy\\mydata3.txt", 
            sep = ' ', row.names = FALSE, col.names = TRUE, quote = FALSE)

```

### EXCEL
```{r out_excel}
write.xlsx(reshapedata3, file = "C:\\Users\\test\\Desktop\\xz\\rstudy\\mydata3.xlsx",
           sheetName="Sheet1",col.names=TRUE, row.names=FALSE, append=FALSE, showNA=TRUE)

```

