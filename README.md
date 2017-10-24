#include<stdio.h>
#include<assert.h>

//限制长度的字符串连接函数
void Mystrncat(char *des,char *src,int count)
{
	char *cp = des;
	assert(src && des);
  
  while(*des != '\0')
	{
		*des++;
	}
  
	while(count && *src)
	{
		*des++ = *src++;
		count--;
	}
	*des = '\0';
	printf("%s\n",cp);
}


int main()
{
  //限制长度字符串连接测试用例
	char str3[20] = {"abc"};
	char *str4 = "xyz";
	Mystrncat(str3,str4,3);
  
  return 0;
}
