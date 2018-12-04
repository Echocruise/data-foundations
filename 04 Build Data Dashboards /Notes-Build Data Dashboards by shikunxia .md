## 数据知识

1. 安斯库姆四重奏（Anscombe's quartet）是四组基本的统计特性一致的数据，但由它们绘制出的图表则截然不同。 每一组数据都包括了11个(x,y)点。
![](https://upload.wikimedia.org/wikipedia/commons/thumb/e/ec/Anscombe%27s_quartet_3.svg/850px-Anscombe%27s_quartet_3.svg.png)
[The Datasaurus Dozen \- Same Stats, Different Graphs: Generating Datasets with Varied Appearance and Identical Statistics through Simulated Annealing \| Autodesk Research](https://www.autodeskresearch.com/publications/samestats)
2. 数据类型
	- discrete 离散数据是数出来的，离散数据只能是某些**既定**的值。
	- continuous 连续数据是测量出来的，连续数据可以是一个范围里**任何**的值
	- categorical 分类数据
	- ordinal 有序变量
3. 图表

- Univariate Plots

	- 单变量定量数据（连续 离散）
		- Histogram 直方图
		- Normal Quantile Plot 正态分布图
		- Stem and Leaf Plot 茎叶图
		- Box and Whisker Plot 箱线图
	- 单变量分类数据 
		- Bar Chart 条形图
		- Pie Chart 饼图
		- Pareto Chart 帕雷多图（频率分布） 	 
	- 对比两个定量数据集 
		- scatter plot 散点图 （Strength+Direction
）
			- Pearson's correlation coefficient
				- A correlation coefficient of 0 doesn't necessarily mean that there is no relationship between two variables. Rather that there isn't a linear relationship.
				- a samller coorelation doesn't mean a weaker relationship
				- correlation coeddicient just could be the 
			- linear relationship 	
			- [科学网—\[转载\]三种相关系数的区别 \- 殷路的博文](http://blog.sciencenet.cn/blog-801621-688307.html)
		- Pie Chart 饼图
		- Pareto Chart 帕雷多图（频率分布） 
		- 时间变化 Line Plots

	[CORREL 函数 \- Office 支持](https://support.office.com/zh-cn/article/correl-%E5%87%BD%E6%95%B0-995dcef7-0c0a-4bed-a3fb-239d7b68ca92)
		
## 数据分析&可视化知识
		
1. Explanatory Analyses
	- Looking for relationships in the data 
	- Connect to questions about data 
	- Visualizations don't need to be perfect 

2. Exploratory Analyses
	- Highlight insight 
	- Surrounded by a story 
	- Do not include unneeded information data analysis process:

3. process

	- Extract - Obtain the data from a spreadsheet, SQL, the web, etc.

	- Clean - Here we could use exploratory visuals.

	- Explore - Here we use exploratory visuals.

	- Analyze - Here we might use either exploratory or explanatory visuals.

	- Share - Here is where explanatory visuals live.


4. visaul encoding 

	- dispaly elements

		- x ,y,color,bars,points,lines,shapes,texture

	- 定量数量
		- position along axis and length

5. poor visualtion

	- lie factor 

	> The “Lie Factor” is a value to describe the relation between the size of effect shown in a graphic and the size of effect shown in the data.
	
	- misleading（人类并不擅长识别基于面积的差别）
	- distract
	- hides


6. chart junk
	- Heavy grid lines
	- Unnecessary text
	- Pictures surrounding the visual
	- Shading or 3d components
	- Ornamented chart axes
7. color
    - start with black and white.
	-  use less intense colors - not all the colors of the rainbow, which is the default in many software applications.
	- Color for communication. Use color to highlight your message and separate groups of interest. Don't add color just to have color in your visualization.
	- use colors on a blue to orange palette.(do not move from red to green )
	
9. extra code 
 - size  size of marker
 - color and shape categorical variables
