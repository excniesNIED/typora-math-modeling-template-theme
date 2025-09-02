# Typora Math Modeling Template

![Typora](https://img.shields.io/badge/Typora-Theme-blue?style=for-the-badge&logo=typora)
![Pandoc](https://img.shields.io/badge/Pandoc-Workflow-orange?style=for-the-badge)
![License](https://img.shields.io/badge/License-MIT-green?style=for-the-badge)

**(English Version Below)**

一份专为**数学建模竞赛（国赛/美赛）** 设计的 Typora 主题和论文排版工作流。

本模板旨在将**内容创作**与**格式排版**彻底分离。你只需要专注于使用 Markdown 撰写论文内容，无需在写作过程中分心于字体、字号和间距的调整。当论文完成后，通过一条简单的命令即可导出符合竞赛格式要求的 Word 文档。

---

## ✨ 功能特性

* **沉浸式写作**：Typora 主题文件 `shumo-paper.css` 提供了高质量的实时预览，让你在写作时就能看到接近最终稿的效果。
* **格式标准化**：严格遵循国赛/美赛对标题、正文、公式、图表的格式要求。
* **一键导出**：基于 Pandoc 和自定义的 Word 参考模板，一键将 `.md` 文件转换为格式规范的 `.docx` 文档。
* **内容与格式分离**：彻底告别在 Word 中反复调整格式的痛苦，让你更专注于模型和求解。
* **跨平台**：无论你使用 Windows, macOS, 还是 Linux，都可以使用本工作流。

## 📁 仓库文件说明

* `shumo-paper.css`: Typora 主题文件，用于写作时的实时预览。
* `reference.docx`: 关键的 Word 参考模板，定义了所有导出所需的样式。
* `README.md`: 本说明文档。

## 🚀 使用流程

### 第 1 步：环境配置

1.  **安装 Typora**: 从 [Typora 官网](https://typora.io/) 下载并安装。
2.  **安装 Pandoc**: 强烈建议从 [Pandoc 官网](https://pandoc.org/installing.html) 下载并安装。Pandoc 是一个强大的文档转换工具，也是本工作流的核心。

### 第 2 步：配置 Typora 主题

1.  打开 Typora，进入 **文件 -> 偏好设置 -> 外观**。
2.  点击 **打开主题文件夹** 按钮。
3.  将本仓库中的 `shumo-paper.css` 文件复制到该文件夹内。
4.  **重启 Typora**。
5.  重启后，从菜单栏的 **主题** 中选择 `Shumo Paper`。

### 第 3 步：撰写论文

现在，你可以开始在 Typora 中撰写你的论文了。所有格式都会实时应用。请注意以下约定：

* **论文题目**：使用 `一级标题` (`# 论文题目`)。
* **一级标题 (如“摘要”、“问题重述”)**：使用 `二级标题` (`## 一级标题`)。
* **二级标题 (如“2.1 模型假设”)**：使用 `三级标题` (`### 二级标题`)。
* **图片标题**：放在图片下方的段落中。
* **表格标题**：放在表格上方的段落中。

### 第 4 步：导出为 Word 文档

1.  将你的论文文件（例如 `paper.md`）和本仓库的 `reference.docx` 文件放在**同一个文件夹**下。
2.  打开命令行终端 (Windows: `cmd` 或 `PowerShell`, macOS: `Terminal`)。
3.  使用 `cd` 命令进入该文件夹。
4.  执行以下命令：
    ```bash
    pandoc paper.md -o final_paper.docx --reference-doc=reference.docx
    ```
    - `paper.md`: 你的 Markdown 源文件名。
    - `final_paper.docx`: 你想要输出的 Word 文件名。
    - `--reference-doc=reference.docx`: 指定使用我们的样式模板。

    执行完毕后，你将得到一个格式完美的 `final_paper.docx` 文件。

### 第 5 步：最终手动调整

打开生成的 `final_paper.docx`，进行竞赛要求的最后几步操作：

1.  **添加承诺书和编号页**：在文档最前面插入两页，分别放入承诺书内容和留作编号页。
2.  **设置页码**：
    * 光标定位到**摘要页**页首。
    * 在 Word 中，**布局 -> 分隔符 -> 下一页**，插入分节符。
    * 双击摘要页的页脚，在工具栏中**取消“链接到前一节”**。
    * **插入 -> 页码 -> 页面底端 -> 居中**。
    * 设置页码格式，使其**起始页码为 1**，并将页码字体设置为 **Times New Roman**。

至此，你的论文已完全符合排版要求！

---

## 📑 具体格式规范

本模板遵循的格式规范如下：

| 项目           | 格式要求                                                     |
| :------------- | :----------------------------------------------------------- |
| **论文题目** | 黑体，四号，居中，与摘要间空 1.5 行                          |
| **一级标题** | 黑体，四号，居中                                             |
| **二级标题** | 黑体，小四，左对齐                                           |
| **摘要** | 从摘要页开始编页码，页脚中部，阿拉伯数字，从“1”开始          |
| **关键词** | 3-5个，分号隔开                                              |
| **正文 (中文)** | 宋体，小四 (12pt)                                            |
| **正文 (西文)** | Times New Roman，小四 (12pt)                                 |
| **段落** | 首行缩进 2 字符，多倍行距 1.25                               |
| **公式** | 独立成行的公式居中，右侧编号 (需在 Markdown 中手动编号，如 `$$...$$ (1)`) |
| **表格** | 经典三线表，标题位于表格上方，居中                           |
| **图片** | 居中放置，标题位于图片下方，居中                             |

## 🤝 贡献与反馈

如果你发现任何问题或有改进建议，欢迎提交 Issue 或 Pull Request！

## 📄 许可证

本项目采用 [MIT License](LICENSE) 开源。

---

## English Version

This is a Typora theme and document generation workflow designed specifically for **Mathematical Modeling Competitions (e.g., MCM/ICM, CUMCM)**.

The core idea is to separate **content creation** from **document formatting**. You can focus on writing your paper in Markdown, without being distracted by fonts, sizes, or spacing. When you're done, a single command exports your work into a competition-ready Word document.

### ✨ Features

* **Immersive Writing**: The `shumo-paper.css` theme provides a high-fidelity live preview in Typora.
* **Standardized Formatting**: Strictly follows the formatting requirements for titles, text, equations, figures, and tables.
* **One-Command Export**: Based on Pandoc and a custom Word reference template, convert `.md` to a perfectly formatted `.docx` file.
* **Separation of Concerns**: Say goodbye to the endless pain of tweaking styles in Word. Focus on your model.
* **Cross-Platform**: Works on Windows, macOS, and Linux.

### 🚀 Workflow

1.  **Setup**: Install [Typora](https://typora.io/) and [Pandoc](https://pandoc.org/installing.html).
2.  **Configure Theme**: Copy `shumo-paper.css` into Typora's theme folder and select the "Shumo Paper" theme.
3.  **Write**: Write your paper in Typora using Markdown.
4.  **Export**: Place your `paper.md` and `reference.docx` in the same folder. Run the following command in your terminal:
    ```bash
    pandoc paper.md -o final_paper.docx --reference-doc=reference.docx
    ```
5.  **Final Touches**: Open the generated `.docx` file. Add the declaration page and numbering page. Insert a section break before the abstract page and set the page number to start from "1".
