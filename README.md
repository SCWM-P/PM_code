# 图片转表格与UML转换器

## 概述

本项目为**22级智能建造工程项目管理大作业**提交项目的代码仓库，是一个基于Gradio的应用程序，它利用大型语言模型的能力将图片转换成表格和UML图。该应用程序旨在处理包含项目管理数据（如活动图）的图片，并将它们输出为结构化的YAML和Markdown格式，同时将它们可视化为UML图。

## 组件

### 1. doubleNumberingNetwork.py

这个Python脚本包含了处理图片和转换格式的核心功能。它使用OpenAI API与语言模型交互，并执行以下任务：

- **上传和提取**：上传图片并使用Kimi API提取内容。
- **YAML和Markdown生成**：将提取的内容转换为YAML文件和Markdown表格。
- **UML转换**：将YAML文件转换为UML图表定义。
- **PERT图生成**：将UML定义转换为PERT图并计算关键路径。

### 2. main.py

该脚本设置了Gradio界面以供用户交互。它处理以下内容：

- **图片上传**：允许用户上传图片进行处理。
- **输出渲染**：显示渲染后的Markdown表格、PlantUML代码和最终的UML图。
- **终端输出**：捕获并显示终端输出，以便透明和调试。

### 3. requirements.txt

列出了运行应用程序所需的所有依赖项。这包括用于图像处理、API交互和Gradio界面创建的库。

### 4. main文件夹

包含了运行该项目所需要的程序库，主要执行由UML代码可视化转化为图表图片的Java文件（已被移到根目录下）及其相关说明和测试样例

## 使用说明

按照以下步骤运行应用程序：

1. **安装依赖项**：运行`pip install -r requirements.txt`安装所有必要的库。
2. **运行应用程序**：执行`python main.py`启动Gradio应用程序。
3. **上传和处理图片**：一旦应用程序运行，上传图片以查看转换过程的实际效果。

## 采用的大模型

本项目采用了兼容[Kimi大模型](https://platform.moonshot.cn/)的API，密钥明文显示在代码中，请在遵守月之暗面公司使用许可的范围内使用该大模型的能力。

## 贡献

本项目的主要贡献成员为TJU 22级智能建造 四名成员，github上考虑到匿名性不做公开。

欢迎E-mail：2251905@tongji.edu.cn，或star这个项目~

## 许可证

该项目是开源的，并在[MIT许可证](LICENSE)下可用。请随意根据许可证条款使用、修改和分发应用程序。
