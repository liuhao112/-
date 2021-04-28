# 排序算法

最近面试经常问到排序算法，部分排序算法了解的不是很清晰，在这里对常用的排序算法整理一下

## 1.冒泡排序

从头开始遍历，每相邻的两个数进行比较，如果符合条件，交换，继续遍历

```markdown
void bubbleSort(vector<int>& value)
{
	for (int i = 0; i < value.size()-1; i++)
	{
		for (int j = 0; j < value.size()-i-1; i++)
		{
			if (value[j] > value[j+1])
			{
				swap(value[j], value[j+1]);
			}
		}
	}
}
```
## 时间复杂度
最坏：数组从大到小排序 o(n*2)\n
最好：数组有序，只需遍历一次O(N)\n

## 2.选择排序法

### 算法步骤
在未排序的序列中找到最小(大)值，置于队列的起始位置
再从剩余未排序序列中找到最小(大)值，置于已排序序列末尾
重复第二部，直到排序结束

### 时间复杂度：
无论序列是否有序，都需要全部遍历找到最小（大）值，复杂度固定为o(n*n)

```
void selectSort(vector<int>& value)
{
	int min = 0;
	for (int i = 0; i < value.size(); i++)
	{
		min = i;  //纪录起始位置
		for (int j = i + 1; j < value.size(); j++)
		{
			if (value[j] < value[min])
			{
				min = j; //纪录更小的位置
			}
		}
    swap(value[i], value[min]); //遍历完后交换
	}
}
```
## 插入排序

### 算法步骤
每个数与已排序的序列依次比较插入到合适的位置




For more details see [GitHub Flavored Markdown](https://guides.github.com/features/mastering-markdown/).

### Jekyll Themes

Your Pages site will use the layout and styles from the Jekyll theme you have selected in your [repository settings](https://github.com/liuhao112/-/settings/pages). The name of this theme is saved in the Jekyll `_config.yml` configuration file.

### Support or Contact

Having trouble with Pages? Check out our [documentation](https://docs.github.com/categories/github-pages-basics/) or [contact support](https://support.github.com/contact) and we’ll help you sort it out.
