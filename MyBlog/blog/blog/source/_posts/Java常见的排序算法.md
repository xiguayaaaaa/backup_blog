---
title: Java常见的排序算法
date: 2022-07-19 20:48:16
tags:
- Java
categories:
- 后端组
cover: 
coverWidth: 1200
coverHeight: 320
author: xiguayaaaaa
from: 
---
 Java常见得的排序算法
 <!--more-->
# Java常见得的排序算法

## 1.冒泡排序

1. 比较相邻的元素。如果第一个比第二个大，就交换他们两个。

2. 对每一对相邻元素放同样的工作，从开始第一对到结尾的最后一对。这步做完后，最后的元素会是最大的数。
3. 针对所有的元素重复以上的步骤，除了最后一个。
4. 持续每次对越来越少的元素重复上面的步骤，直到没有任何一对数字需要比较。

![](https://files.catbox.moe/a0pb5h.gif)

```java
public static void main(String[] args) {
		int[] a = {6,9,7,3,1};
		for (int i = 0; i < a.length-1; i++) {
			for (int j = 0; j < a.length-i-1; j++) {
				if(a[j]>a[j+1]) {
					int temp =a[j];
					a[j] = a[j+1];
					a[j+1] =temp;
				}
			}
		}
		System.out.println(Arrays.toString(a));
}
```

## 2.选择排序

1. 在长度为N的无序数组中，第一次遍历-1个数，找到最小的数与第一个元素交换
2. 第二次遍历-2个数，找到最小的数值与第二个元素交换
3. 重复以上步骤
4. 第n-1次遍历，找到最小的数值与第n-1的元素交换，排序完成

![](https://files.catbox.moe/6jqfd2.gif)

```java
public static void main(String[] args) {
		int[] a = {8,2,3,17,23,85,1,9};
		for (int i = 0; i < a.length; i++) {
            //定义此轮循环最小数放置的位置
            int minIndex = i;
            //从第2个数依次和后面的数进行对比
			for (int j = i+1; j < a.length; j++) {
                //如果minIndex的数比j大则记录j
				if(a[minIndex]>a[j]) {
					minIndex=j;
				}
			}
            if(minIndex!=i){
                int temp = a[minIndex];
                a[minIndex] = a[i];
                a[i] = temp;
                System.out.println("每次结果>>>"+Arrays.toString(a));
            }
			System.out.println("每轮结果==="+Arrays.toString(a));
		}
	}
```

## 3.插入排序

1. 在要排序的无序数组中，假定-1个数已经排好序，现在将第个数插入到前面的有序数列中，使得这个个数也是拍好序的，反复循环，直到全部排好顺序。插入排序也可以理解为从第二个数开始，前面的相邻的数依次两两对比，如果后面的数比前面的数小，则交换位置。(如果实在理解不了，可以类比冒泡排序，把插入排序理解为一种特殊的冒泡排序）

![](https://files.catbox.moe/hzemg8.gif)

```java
public static void main(String[] args) {
		int[] a = {87,86,82,10,30};
		for (int i = 0; i < a.length-1; i++) {
			for (int j = i+1; j >0; j--) {
				if(a[j]<a[j-1]) {
					int temp = a[j];
					a[j] = a[j-1];
					a[j-1] = temp;
				}else{
                	break;   
                }
				System.out.println("每次结果==="+Arrays.toString(a));
			}
			System.out.println("第"+(i+1)+"轮结果>>>"+Arrays.toString(a));
		}
	}
```

## 4.快速排序

快速排序有两种实现方式：双边循环法和挖坑法，思路如下：

##### 快速排序

1. 定义左右指针，并选取一个数作为基准（通常选择数组第一个）
2. 移动右指针，如果右指针的数小于基准数，则停止移动，反之则继续移动
3. 移动左指针，如果左指针的数大于基准数，则停止移动，反之则继续移动
4. 当左右指针都停止移动时交换左右指针处的数
5. 当左右两个指针停在相同位置时，交换指针处的数和基准数的位置
6. 将数组以左右指针位置处一分为二重复上述步骤。

```Java
public class QuickSort {
	/**
	 * 双边循环
	 * @return
	 */
	public static int pivotIndex(int[]ary,int startIndex,int endIndex) {
		//保存左右两个指针，从第一个元素和最后一个元素开始
		int left = startIndex;
		int right = endIndex;
		//获取基准，一般选择数组第一个数
		int pivot = ary[startIndex];
		//大循环，当左右两个指针不相等时，左指针右移，右指针左移
		while (left!=right) {
			//右边指针向左移动，当对应元素大于基准数时继续移动，小于基准数时停止移动
			while(right>left&&ary[right]>=pivot) {
				right--;
			}
			//左边指针向右移动，当小于基准数时继续移动，大于基准数时停止移动
			while (right>left&&ary[left]<=pivot) {
				left++;
			}
			//此时如果左边指针小于右边指针时；左右指针交换元素
			if(left<right) {
				int temp = ary[right];
				ary[right] = ary[left];
				ary[left] = temp;
			}
		}
		int index = left;
		//如果两个指针相等时,交换基准元素和当前位置的数
		ary[startIndex] = ary[index];
		ary[index] = pivot;
		return index;
	}
	public static void qucikSort(int[] ary,int startIndex,int endIndex) {
		if(startIndex>endIndex) {
			return;
		}
		int index = pivotIndex(ary,startIndex,endIndex);
		qucikSort(ary, startIndex, index-1);
		qucikSort(ary, index+1, endIndex);
	}
	public static void main(String[] args) {
		int[] a= {5,6,1,2,4,9,3};
		qucikSort(a, 0, a.length-1);
		System.out.println(Arrays.toString(a));
	}
}
```

##### 挖坑法

1. 选取起始位置作为标记位（也就是坑），选取一个数作为基准，通常是数组第一个
2. 从数组第二数开始依次和基准数对比，如果比基准数小，则扩大小于基准数的区间，也就是mark++,并将该数与标mark处的数交换
3. 循环结束后，将mark处的数和基准数进行交换
4. 以mark为界，将数组一分为二重复上述步骤

![](https://files.catbox.moe/dcwsxe.gif)

```Java
/**
 * 单边循环
 * @author MR.W
 */
public class QucikSort2 {
	public static int pivotIndex(int[] ary,int startIndex,int endIndex) {
		int mark = startIndex;
		int pivot = ary[startIndex];
		for (int i = startIndex+1; i <= endIndex; i++) {
			//如果指针指向的元素小于基准元素，干两件事情
			//1.mark+1,扩大小于基准数的区间
			//2.将指针所指向的数和mark位置处的数进行交换
			if(ary[i]<pivot) {
				mark++;
				int temp = ary[i];
				ary[i] = ary[mark];
				ary[mark] = temp;
			}
		}
		//当循环结束时将mark位置的数和基准数进行交换
		ary[startIndex]= ary[mark]; 
		ary[mark] = pivot;
		return mark;
	}
	public static void quickSort(int[] ary,int startIndex,int endIndex) {
		if(startIndex>endIndex) {
			return;
		}
		int index = pivotIndex(ary, startIndex, endIndex);
		quickSort(ary, startIndex, index-1);
		quickSort(ary, index+1, endIndex);
	}
	public static void main(String[] args) {
		int [] a = {7,9,1,4,8};
		quickSort(a, 0, a.length-1);
		System.out.println(Arrays.toString(a));
	}
}
```

```java
public static void main(String[] args) {
		
		int [] a = {5,1,6,2,3};
		
		for (int i = 0; i < a.length; i++) {
			for (int j = 0; j < a.length-1; j++) {
				int temp;
				if(a[i]<a[j]) {
					temp = a[j];
					a[j] = a[i];
					a[i] = temp;
				}
				System.out.println("每次"+Arrays.toString(a));
			}
			System.out.println("每轮"+Arrays.toString(a));
		}
		System.out.println("最后"+Arrays.toString(a));
	}
```

