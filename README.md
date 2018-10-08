0.冒泡排序
思路：(考虑N个数,N=10) 
(1)将待排序的N个数放入数组：num[1]..num[N-1].
(2)从0到N-1相邻的两个数依次比较，(1)将待指序的N个数放人数  I num中，比较保证小数在前、大数在后。此次比较结果
num[ N-1]中的数是数组中最大的数。
(3)余下N-1个元素。
(4)从0到下_2本的两个数依次比较，小数在前大数在后.此次numn[N-2]是N-1A元素中最大。
..
(5)num[O]与num[1]比较，num[ 1]存大数。(6) num[0]存最小数，比较结束。
代码：
#include<stdio.h>
#include<stdlib.h>
#pragma warning(disable:4996)
#define N 10
void main()
{
	int i,j,t,num[N];
	for(i=0;i<N;i++)
		scanf("%d",&num[i]);
	for(i=1;i<N;i++)
	{
		for(j=0;j<N-i;j++)
		{
			if(num[j]>num[j+1])
			{
				t=num[j];
				num[j]=num[j+1];
				num[j+1]=t;
			}
		}
	}
	for(i=0;i<N;i++)
		printf("%5d",num[i]);
	system("pause");
	return;
}
