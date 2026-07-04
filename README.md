# materials-science-gallery
该仓库根据上海交通大学版《材料科学基础》教材，通过LaTeX中的TikZ宏包对书中部分图表进行矢量化重绘制，并原图基础上适当增加了部分内容使之更加易懂。该仓库中的代码主要来源于作者的《材料科学基础》笔记，未经专业人员勘误，部分内容可能存在学术上的谬误，欢迎提交Issue 或 Pull Request 来修正图表中的学术错误，或者贡献更多材料科学领域的经典 TikZ 图表！
## 🌟 项目特点

- **矢量图**：全部基于原生 TikZ 宏包绘制，图像可无损缩放。
- **独立编译**：所有图表均使用 `standalone` 文档类进行源码分离，支持单独编译输出 PDF/PNG，也支持无缝嵌入主文档。

## 🛠️ 编译环境与依赖

为了能够成功编译本仓库的 `.tex` 源码，请确保你的 TeX 环境满足以下条件：

- **编译器**：由于代码中包含中文标注，**务必使用 `XeLaTeX`** 进行编译。
- **宏包**：参见具体源代码所需的宏包。

## 🚀 使用方法

### 方法一：单独编译出图
直接使用你的 LaTeX 编辑器（如 VS Code、TeXstudio）打开对应的 `.tex` 文件，选择 `XeLaTeX` 编译器编译，即可获得一张完美裁剪、无白边的 PDF 矢量图片。

### 方法二：在你的 LaTeX 主文档中引入
1. 将对应的 `.tex` 文件复制到你的排版项目目录下。
2. 在你的主文档导言区加入有关宏包：
   ```latex
   \usepackage{standalone}
   \usepackage{tikz}
   \usepackage{tikz-cd}
   ...
3. 在正文中使用`\input`插入：
   ```latex
   \begin{figure}[htbp]
   \centering
   \input{fig} % 不需要写 .tex 后缀
   \caption{图表名称}
   \end{figure}
