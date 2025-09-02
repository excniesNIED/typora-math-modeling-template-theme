# Math Modeling Paper Templates for Typora

![Typora](https://img.shields.io/badge/Typora-Themes-blue?style=for-the-badge&logo=typora)
![Pandoc](https://img.shields.io/badge/Pandoc-Workflow-orange?style=for-the-badge)
![Contest](https://img.shields.io/badge/MCM/ICM-CUMCM-brightgreen?style=for-the-badge)
![License](https://img.shields.io/badge/License-MIT-green?style=for-the-badge)

**(English Version Summary Below)**

一份专为**数学建模竞赛**设计的 Typora 主题与论文排版工作流**集合**。

本仓库旨在将**内容创作**与**格式排版**彻底分离，让你无论是参加**国赛 (CUMCM)** 还是**美赛 (MCM/ICM)**，都能使用 Markdown 高效写作，并通过一条命令导出符合相应竞赛格式的 Word 文档。

---

## ✨ 功能特性

* **双主题支持**：内置 `cumcm-paper.css` (国赛) 和 `mcm-paper.css` (美赛) 两个独立主题，提供精准的实时预览。
* **格式标准化**：严格遵循两大竞赛对标题、正文、字体、图表的官方格式要求。
* **一键导出**：基于 Pandoc 和定制化的 Word 参考模板，一键将 `.md` 文件转换为格式规范的 `.docx` 文档。
* **内容与格式分离**：彻底告别在 Word 中反复调整格式的痛苦，让你更专注于模型和求解。
* **跨平台**：无论你使用 Windows, macOS, 还是 Linux，都可以使用本工作流。

## 📁 仓库文件说明

* **主题文件 (Themes):**
    * `cumcm-paper.css`: **国赛 (CUMCM)** 专用 Typora 主题。
    * `mcm-paper.css`: **美赛 (MCM/ICM)** 专用 Typora 主题。
* **参考模板 (Reference Docs):**
    * `reference-cumcm.docx`: **国赛** Word 导出样式模板。
    * `reference-mcm.docx`: **美赛** Word 导出样式模板。
* `README.md`: 本说明文档。

## 🚀 通用工作流程

无论参加国赛还是美赛，基本流程是相同的。

### 第 1 步：环境配置

1.  **安装 Typora**: 从 [Typora 官网](https://typora.io/) 下载并安装。
2.  **安装 Pandoc**: 强烈建议从 [Pandoc 官网](https://pandoc.org/installing.html) 下载并安装，这是实现一键导出的核心工具。

### 第 2 步：配置 Typora 主题

1.  打开 Typora，进入 **文件 -> 偏好设置 -> 外观 -> 打开主题文件夹**。
2.  将本仓库中的 `cumcm-paper.css` 和 `mcm-paper.css` **两个文件**都复制进去。
3.  **完全关闭并重启 Typora**。
4.  重启后，从菜单栏的 **主题** 中根据你的需要选择 `CUMCM Paper` 或 `MCM Paper`。

### 第 3 步：撰写论文

在选定的主题下，使用 Markdown 撰写论文。**请务必参考下方不同竞赛的《格式规范与写作约定》**，以确保 Markdown 标签（如`#`, `##`）能被正确渲染和导出。

### 第 4 步：一键导出为 Word 文档

这是最关键的一步。确保你的论文 `.md` 文件与相应的 `.docx` 参考模板放在**同一个文件夹**下。

#### 导出美赛 (MCM/ICM) 格式 🇺🇸

打开命令行终端，进入文件所在目录，执行：
```bash
pandoc your-paper.md -o final-mcm.docx --reference-doc=reference-mcm.docx
```

#### 导出国赛 (CUMCM) 格式 🇨🇳

打开命令行终端，进入文件所在目录，执行：
```bash
pandoc your-paper.md -o final-cumcm.docx --reference-doc=reference-cumcm.docx
```

### 第 5 步：最终手动调整

导出后的 Word 文档已完成 95% 的工作。你只需进行少量最终调整：

* **国赛**: 按要求添加承诺书、编号页，并从摘要页开始设置页码。
* **美赛**: 添加官方要求的 Summary Sheet 和目录，并根据要求设置页码。

---

## 📑 格式规范与写作约定

### 🇺🇸 美赛 (MCM/ICM) 格式规范

| 项目         | 格式要求                                   |
| :----------- | :----------------------------------------- |
| **摘要标题** | `Abstract`: Arial, 小三 (15pt), 粗体, 居中 |
| **关键词**   | `Key words`: Arial, 四号 (14pt), 粗体      |
| **一级标题** | Times New Roman, 小二 (18pt), 粗体         |
| **二级标题** | Times New Roman, 三号 (16pt), 粗体         |
| **三级标题** | Times New Roman, 四号 (14pt), 粗体         |
| **正文**     | Times New Roman, 12pt, 1.5倍或2倍行距      |
| **页码**     | 页面底部中间或右侧                         |

#### **美赛写作约定 (重要!)**
* **摘要标题 `Abstract`**: 使用 **一级标题** (`# Abstract`)
* **一级标题 (如 `1. Introduction`)**: 使用 **二级标题** (`## 1. Introduction`)
* **二级标题 (如 `1.1 Assumptions`)**: 使用 **三级标题** (`### 1.1 Assumptions`)
* **三级标题 (如 `1.1.1 Data`)**: 使用 **四级标题** (`#### 1.1.1 Data`)
* **关键词 `Key words`**: 使用 **五级标题** (`##### Key words:`)

---

### 🇨🇳 国赛 (CUMCM) 格式规范

| 项目                 | 格式要求                               |
| :------------------- | :------------------------------------- |
| **论文题目**         | 黑体, 四号, 居中                       |
| **一级标题**         | `摘要`/`问题重述`等: 黑体, 四号, 居中  |
| **二级标题**         | `2.1 模型假设`: 黑体, 小四, 左对齐     |
| **正文 (中文)**      | 宋体, 小四 (12pt)                      |
| **正文 (西文/数字)** | Times New Roman, 小四 (12pt)           |
| **段落**             | 首行缩进2字符, 多倍行距 1.25           |
| **页码**             | 从摘要页开始, 页脚中部, 阿拉伯数字 "1" |

#### **国赛写作约定 (重要!)**
* **论文题目**: 使用 **一级标题** (`# 你的论文题目`)
* **一级标题 (如 `摘要`, `问题重述`)**: 使用 **二级标题** (`## 摘要`)
* **二级标题 (如 `2.1 模型假设`)**: 使用 **三级标题** (`### 2.1 模型假设`)
* **三级及以下标题**: 使用 `####` 等即可。

## 🤝 贡献与反馈

如果你发现任何问题或有改进建议，欢迎提交 Issue 或 Pull Request！

## 📄 许可证

本项目采用 [MIT License](LICENSE) 开源。

---
## English Version Summary

This repository provides an all-in-one toolkit for academic writing in major mathematical modeling competitions. It includes:

* **Two distinct Typora themes**: `mcm-paper.css` for the US Contest (MCM/ICM) and `cumcm-paper.css` for the China Contest (CUMCM).
* **Two corresponding Word reference templates**: `reference-mcm.docx` and `reference-cumcm.docx` for high-quality export.
* **A unified workflow**:
    1.  Install Typora and Pandoc.
    2.  Copy the CSS files to Typora's theme folder and select the one you need.
    3.  Write your paper in Markdown, following the conventions detailed above for your specific contest.
    4.  Use the appropriate Pandoc command to export your `.md` file to a beautifully formatted `.docx` document.
    5.  Perform minor manual adjustments in Word (e.g., adding cover pages and setting page numbers).

This toolkit separates content from formatting, allowing you to focus on what truly matters: your model and your solution.
