# ACM-
ACM题目练习

/*题意：有 10 个英文字母（包含大小写），用计算机实现以下功能。把这 10 个字母按英文
字母 A,B,C„„,Z， a,b,c,„„,z 顺序排序并输出。注意：小写字母应该在大写字母的后
面。
输入：任意输入 10 个英文字母。
输出：这 10 个字母排序后的序列。*/

#include<stdio.h>

int main()
{
	char arr[11], ch;

	scanf("%s", arr);

	for(int i = 0; i < 10; i++)
	{
		for(int j = 0; j < 9; j++)
		{
	    	if(arr[j] > arr[j+1])
			{
		    	ch = arr[j];
		    	arr[j] = arr[j+1];
		    	arr[j+1] = ch;
			}
		}
	}

	printf("%s\n", arr);

	return 0;
}
