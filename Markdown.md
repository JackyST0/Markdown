# Markdown 标题:  
* ## 使用 = 和 - 标记一级和二级标题
  ### = 和 - 标记语法格式如下：
  ```
  我展示的是一级标题
  =================

  我展示的是二级标题  
  -----------------
  ```
* ## 使用 # 号标记  
  ### 使用 # 号可表示 1-6 级标题，一级标题对应一个 # 号，二级标题对应两个 # 号，以此类推。
  ```
  # 一级标题
  ## 二级标题
  ### 三级标题
  #### 四级标题
  ##### 五级标题
  ###### 六级标题
  ```
# Markdown 段落：
#### Markdown 段落没有特殊的格式，直接编写文字就好，段落的换行是使用两个以上空格加上回车。
 
* ## 字体
  ### Markdown 可以使用以下几种字体：
  ```
  *斜体文本*
  _斜体文本_
  **粗体文本**
  __粗体文本__
  ***粗斜体文本***
  ___粗斜体文本___
  ```
* ## 分隔线
  ### 你可以在一行中用三个以上的星号、减号、底线来建立一个分隔线，行内不能有其他东西。你也可以在星号或是减号中间插入空格。下面每种写法都可以建立分隔线：
  ```
  ***

  * * *

  *****

  - - -

  ----------
  ```
* ## 删除线
  ### 如果段落上的文字要添加删除线，只需要在文字的两端加上两个波浪线 ~~ 即可，实例如下：
  ```
  RUNOOB.COM
  GOOGLE.COM
  ~~BAIDU.COM~~
  ```
* ## 下划线
  ### 下划线可以通过 HTML 的 `<u>` 标签来实现：
  ```
  <u>带下划线文本</u>
  ```
* ## 脚注
  ### 脚注是对文本的补充说明，Markdown 脚注的格式如下：
  ```
  [^要注明的文本]
  ```
  ### 以下实例演示了脚注的用法：
  ```
  创建脚注格式类似这样 [^RUNOOB]。

  [^RUNOOB]: 菜鸟教程 -- 学的不仅是技术，更是梦想！！！
  ```
# Markdown 列表：
* ## Markdown 支持有序列表和无序列表。
  ### 无序列表使用星号(*)、加号(+)或是减号(-)作为列表标记，这些标记后面要添加一个空格，然后再填写内容：
  ```
  * 第一项
  * 第二项
  * 第三项

  + 第一项
  + 第二项
  + 第三项


  - 第一项
  - 第二项
  - 第三项
  ```
  ### 有序列表使用数字并加上 . 号来表示，如：
  ```
  1. 第一项
  2. 第二项
  3. 第三项
  ```
* ## 列表嵌套
  ### 列表嵌套只需在子列表中的选项前面添加两个或四个空格即可：
  ```
  1. 第一项：
      - 第一项嵌套的第一个元素
      - 第一项嵌套的第二个元素
  2. 第二项：
      - 第二项嵌套的第一个元素
      - 第二项嵌套的第二个元素
  ```
# Markdown 区块：
* ## 区块引用
  ### Markdown 区块引用是在段落开头使用 > 符号 ，然后后面紧跟一个空格符号：
  ```
  > 区块引用
  > 菜鸟教程
  > 学的不仅是技术更是梦想
  ```
  ### 另外区块是可以嵌套的，一个 > 符号是最外层，两个 > 符号是第一层嵌套，以此类推：
  ```
  > 最外层
  > > 第一层嵌套
  > > > 第二层嵌套
  ```
* ## 区块使用列表
  ### 区块中使用列表实例如下：
  ```
  > 区块中使用列表
  > 1. 第一项
  > 2. 第二项
  > + 第一项
  > + 第二项
  > + 第三项
  ```
* ## 列表中使用区块
  ### 如果要在列表项目内放进区块，那么就需要在 > 前添加四个空格的缩进，列表中使用区块实例如下：
  ```
  * 第一项
      > 菜鸟教程
      > 学的不仅是技术更是梦想
  * 第二项
  ```
# Markdown 代码：
* ## 函数代码
  ### 如果是段落上的一个函数或片段的代码可以用反引号把它包起来（`），例如：
  ```
  `printf()` 函数
  ```
* ## 代码区块
  ### 代码区块使用 4 个空格或者一个制表符（Tab 键）。
      $(document).ready(function () {
          alert('RUNOOB');
      });
  ### 你也可以用 \` \` \` 包裹一段代码，并指定一种语言（也可以不指定）：
  ```
  $(document).ready(function () {
      alert('RUNOOB');
  });
  ```
# Markdown 链接：
* ## 链接使用方法如下：
  ```
  [链接名称](链接地址)

  或者

  <链接地址>
  ```
  ### 例如：
  ```
  这是一个链接 [百度](https://www.baidu.com)
  ```
  ### 直接使用链接地址：
  ```
  <https://www.runoob.com>
  ```
* ## 高级链接
  ### 我们可以通过变量来设置一个链接，变量赋值在文档末尾进行：
  ```
  这个链接用 1 作为网址变量 [Google][1]
  这个链接用 runoob 作为网址变量 [Runoob][runoob]
  然后在文档的结尾为变量赋值（网址）

  [1]: http://www.google.com/
  [runoob]: http://www.runoob.com/
  ```
# Markdown 图片：
* ## Markdown 图片语法格式如下：
  ```
  ![alt 属性文本](图片地址)

  ![alt 属性文本](图片地址 "可选标题")
  
  1. 开头一个感叹号 !
  2. 接着一个方括号，里面放上图片的替代文字
  3. 接着一个普通括号，里面放上图片的网址，最后还可以用引号包住并加上选择性的 'title' 属性的文字。
  ```
  ### 使用实例：
  ```
  ![RUNOOB 图标](http://static.runoob.com/images/runoob-logo.png)

  ![RUNOOB 图标](http://static.runoob.com/images/runoob-logo.png "RUNOOB")
  ```
  ### 当然，你也可以像网址那样对图片网址使用变量:
  ```
  这个链接用 1 作为网址变量 [RUNOOB][1].
  然后在文档的结尾为变量赋值（网址）

  [1]: http://static.runoob.com/images/runoob-logo.png
  ```
  ### Markdown 还没有办法指定图片的高度与宽度，如果你需要的话，你可以使用普通的 `<img>` 标签。
  ```
  <img src="http://static.runoob.com/images/runoob-logo.png" width="50%">
  ```
# Markdown 表格：
* ## 制作表格
  ### Markdown 制作表格使用 | 来分隔不同的单元格，使用 - 来分隔表头和其他行，语法格式如下：
  ```
  |  表头   | 表头  |
  |  ----  | ----  |
  | 单元格  | 单元格 |
  | 单元格  | 单元格 |
  ```
* ## 对齐方式
  ### 我们可以设置表格的对齐方式：
  ```
  -: 设置内容和标题栏居右对齐。
  :- 设置内容和标题栏居左对齐。
  :-: 设置内容和标题栏居中对齐。
  ```
  ### 实例如下：
  ```
  | 左对齐 | 右对齐 | 居中对齐 |
  | :-----| ----: | :----: |
  | 单元格 | 单元格 | 单元格 |
  | 单元格 | 单元格 | 单元格 |
  ```
# Markdown 注释:
* ## 使用原生 HTML 注释语法
  ### 通过 html 的 `<!-- -->` 标记实现文档注释效果:
  ```
  #### 基于 HTML 标签的注释

  <!-- 这是一段被注释掉的文字 -->

  这是一段没有被注释的文字
  ```
* ## 使用 HTML 样式实现隐藏
  ### 通过将 html 样式设置成 `display:none`，以达到注释效果:
  ``` 
  #### 基于 HTML 样式

  <div style="display:none">
  这是一段被注释掉的文字
  </div>

  这是一段没有被注释的文字
  ```
* ## 通过 Markdown 自身的解析功能　　
  ### 这种方法是利用了 Markdown 自身的语法，在"链接"章节的内容中提到过可以通过 `中括号 []` 的方式定义全局链接，而这种方式声明的内容不会被渲染成文字内容输出，因此达到了注释的效果。
  ```
  #### 通过 Markdown 解析达到注释效果

  [//]: (这是一段被注释掉的文字)

  这是一段没有被注释的文字
  ```
# Markdown 高级技巧：
* ## 支持的 HTML 元素
  ### 不在 Markdown 涵盖范围之内的标签，都可以直接在文档里面用 HTML 撰写，目前支持的 HTML 元素有：`<kbd>` `<b>` `<i>` `<em>` `<sup>` `<sub>` `<br>` 等 ，如：  
  ```
  使用 <kbd>Ctrl</kbd>+<kbd>Alt</kbd>+<kbd>Del</kbd> 重启电脑
  ```
* ## 转义
  ### Markdown 使用了很多特殊符号来表示特定的意义，如果需要显示特定的符号则需要使用转义字符，Markdown 使用反斜杠转义特殊字符：
  ```
  **文本加粗** 
  \*\* 正常显示星号 \*\*
  ```
  ### Markdown 支持以下这些符号前面加上反斜杠来帮助插入普通的符号：
  ```
  \   反斜线
  `   反引号
  *   星号
  _   下划线
  {}  花括号
  []  方括号
  ()  小括号
  #   井字号
  +   加号
  -   减号
  .   英文句点
  !   感叹号
  ```
* ## 公式
  ### Markdown Preview Enhanced 使用 KaTeX 或者 MathJax 来渲染数学表达式。KaTeX 拥有比 MathJax 更快的性能，但是它却少了很多 MathJax 拥有的特性。你可以查看 KaTeX supported functions/symbols 来了解 KaTeX 支持那些符号和函数，默认下的分隔符：
  ```
  $...$ 或者 \(...\) 中的数学表达式将会在行内显示。
  $$...$$ 或者 \[...\] 或者 ```math 中的数学表达式将会在块内显示。
  ```
  
  $$
  \begin{Bmatrix}
     a & b \\
     c & d
  \end{Bmatrix}
  $$
  $$
  \begin{CD}
     A @>a>> B \\
  @VbVV @AAcA \\
     C @= D
  \end{CD}
  $$

* ## 以下几个实例效果图如下：
  ### 1、横向流程图源码格式：
  ```mermaid
  graph LR
  A[方形] -->B(圆角)
      B --> C{条件a}
      C -->|a=1| D[结果1]
      C -->|a=2| E[结果2]
      F[横向流程图]
  ```
  ### 2、竖向流程图源码格式：
  ```mermaid
  graph TD
  A[方形] --> B(圆角)
      B --> C{条件a}
      C --> |a=1| D[结果1]
      C --> |a=2| E[结果2]
      F[竖向流程图]
  ```

