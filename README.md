# funtion-search
A faster and more distinct searching method. Compared with traditional searching methods, this code provides a way to find the index directly through the target value, which greatly increases the searching speed and reduces memory usage. It can be nearly twice as fast as the original binary search when dealing with large datasets.

## 🌟 Core Features
A faster and more innovative searching method. Compared to traditional search methods, this code provides a way to find indices directly through target values. It significantly reduces search time and memory usage, being nearly twice as fast as the original binary search when dealing with large datasets.

For searching within a sorted dataset, if the target number exists, it will be located within a certain interval of the dataset. This code uses a function to narrow down this interval, and finally performs binary search or other searches within this interval to achieve faster query speed.

There is a function whose graph approximates the trend of the data. The maximum error (△max) is the maximum value among all differences between the function's y-value at x (where x is the index of the data) and the actual value of the data. For example, with the function y=x, if there is a data value of 3 at index x=5, then △ is |5-3|. We calculate all such △ values and find the maximum one, which is △max.

After determining △max, when searching for an unknown target value in the dataset, we can narrow down the range to target ± △max. The final interval size, and thus the final query speed, depends on △max.

This method is suitable for large, sorted datasets with relatively stable data changes. For such data, it can be nearly twice as fast as the original binary search method.

Different datasets can be fitted using functions like lnx, x, e^x-1, or others. For data with exponential growth or growth that later stabilizes, exponential functions can be used for fitting. However, the fitting must reduce △max; otherwise, it will have no effect. For flat data regions, a larger △max will lead to a sharp increase in the number of indices included in the final range, thereby affecting query efficiency. Any fitting function aims to reduce △max. If it cannot reduce △max, there is no need to use nonlinear equations for fitting, as this would only increase the difficulty of calculating the final target interval indices.

## 🚀 Quick Start
Download the src folder and copy it into a Java project. Run the classes in sequence (GenerateLinearData -> LinearFitter -> Main) to test directly.

#介绍
  更快，更不一样的查找方法，相较于传统查找方法，该代码提供了一种直接通过目标值来找到索引的方法。极大减少了查找速度，以及内存占用。比原有二分查找在数据量大的情况下可快近乎一倍。
## 🌟 核心功能

  对于一组排序好的数据的查找，目标数如果存在，就会位于这组数据的某个区间，该代码提供了一种通过函数来缩小这个区间，最后在这个区间内进行二分查找或其他查找以达到更快速地查询。
  现有一个函数，其图像趋近于数据走向，最大误差（所有 函数在x=数据所在x的y值 与 数据真实值的差 的最大值）为△max，比如有函数y=x,在索引x=5处有一个数据3，则△为|5-3|，计算出所有△并找出最大值△max。
  找出△max后，要查找某一个未知数据target是否在组数据中，可以把范围缩小到targer±△max，最终区间大小，也就是最终查询速率，取决于△max。
该方法适用于排序好，数据变化量较平稳，数据量大的数据。对于此类数据，相较于原二分查找法能快近乎一倍的速度。
对于不同的数据组，可以用lnx，x，e^x-1或其他函数来拟合。对于指数增长或者增长后又趋于平稳的属性形态，可以用指数型函数来拟合，不过拟合必须能够降低其△max，否则没有任何效果。对于数据平缓区来说，较大的△max会导致最终范围包含的index索引数量剧增，从而影响查询效率。任何拟合函数，都是为了降低△max，如果无法降低△max，便没必要用非线性方程进行拟合，加大最终目标区间索引的计算难度。


## 🚀 快速开始
下载该src后复制进一个java项目，按顺序运行类(运行顺序GenerateLinearData -> LinearFitter -> Main)便可直接测试


