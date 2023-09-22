# Timeline Beta

此项目是将 [TimelineJS3](https://github.com/NUKnightLab/TimelineJS3) 移植为[思源笔记](https://github.com/siyuan-note/siyuan)挂件。

反馈可在 [Issues · choyy/Timeline-SY](https://github.com/choyy/Timeline-SY/issues) 或 [[挂件] 时间线 - 链滴](https://ld246.com/article/1653294035002/comment/1662474726531#comments) 。

## 预览

![](https://b3logfile.com/file/2022/06/preview-b9ad35d5.png?imageView2/2/interlace/1/format/webp)

## 使用说明

* **界面介绍**

  界面分为上、下两部分，上方为时间轴，时间轴上显示所创建的事件和时期；下方为幻灯片，点击时间轴上的事件或时期即可展示其具体内容。
* **时间线内容组成：** 标题、事件、时期和纪元

  * 标题是用来描述该时间线的主题，一个时间线仅有一个标题，不可删除。
  * 事件是对应某一时间点的项目，在时间轴上占据某一时间点。
  * 时期是对应某一时间段的项目，在时间轴上占据某一时间段。
  * 纪元与时期类似，同样对应某一时间段，它是简化版的时期，仅由开始时间、结束时间和名称组成。与时期相比，纪元更加简洁，它直接显示在时间轴上，对于一段很长的时期使用纪元可能效果更好，比如使用“第二次世界大战”纪元：
    ![图片.png](https://b3logfile.com/file/2022/08/图片-f920b38a.png)
* **时间线编辑操作：** 新建、编辑和删除

  * 新建：点击新建按钮可新建一个项目，其中**开始日期**和**标题**为必填项，结束日期、描述、分组、背景图片和思源块 id 为选填项。
    * 若结束日期留空，则表示该项目为一个事件，否则表示一个时期。
    * 标题会在时间轴中显示，在标题开头使用颜色标记可给标题指定颜色，有 6 种颜色标记可选：#r(红色)、#g(绿色)、#b(蓝色)、#y(黄色)、#o(橙色)、#p(紫色)
    ![](https://b3logfile.com/file/2022/08/图片-b5893a04.png)
    * 描述为对该时间或时期的具体描述。

      标题与描述支持使用 **markdown 语法插入网页链接**
    * 分组用于对事件进行分类，给事件添加一个分组，同一分组的事件会在时间轴上显示在同一行
    * 背景图片为该事件或时期对应幻灯片的背景，背景图片须填入图片的 url ，也可为思源的资源文件，格式为 `assets/xxx.jpg/png`。

    ![image.png](https://b3logfile.com/file/2022/08/图片-1b035ec3.png)
  * 编辑：点击编辑按钮可编辑当前幻灯片所对应的事件或时期的内容。
  * 删除：点击编辑按钮可编辑当前幻灯片所对应的事件或时期，注意当时间轴上仅有一个事件或时期时无法删除，因为时间轴上至少要有一个项目。
  * 可在浏览器打开时间线进行编辑操作，在浏览器编辑后需在思源中刷新时间线才能看到浏览器编辑后的内容。

* **嵌入或链接到思源内容块**

  * **链接**：**描述**支持粘贴**思源块超链接**,粘贴思源块超链接不影响输入其他内容，保存后点击链接即可跳转到对应块。
    
    同时，**思源块超链接**同样支持 markdown 链接语法，可通过`[锚文本](思源块超链接)`语法插入超链接。
    ![image.png](https://b3logfile.com/file/2022/06/%E5%9B%BE%E7%89%87-f36db112.png?imageView2/2/interlace/1/format/webp)

  * **嵌入**：在**思源块id**填入 id 即可在幻灯片嵌入该内容块。
    ![image.png](https://b3logfile.com/file/2022/06/embedblock-14d6ed31.png?imageView2/2/interlace/1/format/webp)

* **数据存储：** 时间线数据存储在挂件块的自定义属性中，建议将数据做个备份以防不测。

## 感谢

[NUKnightLab](https://github.com/NUKnightLab) 的 [TimelineJS3](https://github.com/NUKnightLab/TimelineJS3)

感谢 [leolee9086](https://github.com/leolee9086) 提供的帮助以及贡献了“嵌入思源内容块"功能

感谢**池鱼**以及 [Zuoqiu-Yingyi](https://github.com/Zuoqiu-Yingyi) 提供的帮助

## 更新日志

- 20230421：v0.0.16，支持时、分、秒
- 20230421：v0.0.14，支持全屏，修复#17
- 20220906：v0.0.13，修复移动端无法显示的bug
- 20220819：v0.0.12，支持分组重命名
- 20220810：v0.0.11，新增分组、时间线设置、给时间轴上项目标题添加颜色
- 20220701：v0.0.10，新增“纪元”
- 20220618：v0.0.9，新增刷新时间线，在浏览器编辑后在思源中刷新才能看到
- 20220614：v0.0.8，支持鼠标滚轮切换幻灯片
- 20220530：v0.0.7，支持直接插入思源块超链接，支持markdown语法插入思源块超链接
- 20220527：v0.0.6，描述支持换行，删除时自动跳到下一个
- 20220525：v0.0.5，支持嵌入思源内容块
- 20220524：v0.0.4，支持链接到思源内容块，支持markdown语法链接