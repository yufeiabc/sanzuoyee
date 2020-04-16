#include<stdio.h>
#include<stdlib.h>
#include <iostream>
#include <string>
using namespace std;
int top=0;
struct xingxi{//学生
	char name[20];//学生姓名
	char num[20];//学生学号
	char clas[20];//学生班级
}stu[20];
struct pingjia{//老师
	char name[20];//老师姓名
	char course[20];//课程
	int beike;//备课情况
	int hudong;//互动情况
	int keliang;//授课信息量
	int liuli;//上课是否流利
	int jiqing;//上课是否有激情
	int qifa;//是否启发教学
	int average;//平均分
}tea[20];

void inputs()
{
	int i;top++;
	cout<<"请输入您的姓名：";
	
	cin>>stu[top].name;

	cout<<"请输入您的学号：";
	cin>>stu[top].num;
	cout<<"请输入您的班级：";
	cin>>stu[top].clas;
	cout<<"登陆成功！";
}
void inputt(int n)//输入老师的信息
{
     int i;
	 for(i=0;i<n;i++)
	 {

         cout<<"请输入老师的姓名";
	     cin>>tea[i].name;
	     cout<<"请输入老师的课程";
	     cin>>tea[i].course;
	     

	 }
	 cout<<"开始评价!";
}
void evalu(int n)//为老师打分
{
	for(int i=0;i<n;i++)

	{
	 printf("请为%s老师打分]\n",tea[i].name);
	cout<<"请为教师备课情况打分（0-100）";
	cin>>tea[i].beike;
	cout<<"请为教师互动情况打分(0-100)";
	cin>>tea[i].hudong;
	cout<<"请为教师授课信息量打分(0-100)";
	cin>>tea[i].keliang;
	cout<<"请为教师上课是否流利打分(0-100)";
	cin>>tea[i].liuli;
	cout<<"请为教师上课是否有激情打分(0-100)";
	cin>>tea[i].jiqing;
	cout<<"请为教师是否启发教学打分(0-100)";
	cin>>tea[i].qifa;
	}
}
void zui(int n)//求平均分
{
	int ave;
	for(int i=0;i<n;i++)
	{
	ave=(tea[i].beike+tea[i].hudong+tea[i].keliang+tea[i].liuli+tea[i].jiqing+tea[i].qifa)/6;
    tea[i].average=ave;
	}
}
void paixu(int n)//排序
{
	int i,j;struct pingjia temp;
	for(i=0;i<n-1;i++)
	{
		for(j=0;j<n-i+1;j++)
		{
			if(tea[j].average<tea[j+1].average)
			{
				temp=tea[j];
				tea[j]=tea[j+1];
				tea[j+1]=temp;
			}
		}
	}
	for(i=0;i<n;i++)
	{
		cout<<tea[i].name<<' '<<tea[i].course<<' '<<tea[i].beike<<' '<<tea[i].hudong<<' '<<tea[i].keliang<<' '<<tea[i].liuli<<' '<<tea[i].jiqing<<' '<<tea[i].qifa<<' '<<tea[i].average;
		cout<<'\n';
	}
}
int chaxun(int n,char nam[])//查询
{
	int i,flag=0;
	for(i=0;i<n;i++)
	{
		if(strcmp(tea[i].name,nam)==0)
		{
			flag=1;
		   cout<<tea[i].name<<' '<<tea[i].course<<' '<<tea[i].beike<<' '<<tea[i].hudong<<' '<<tea[i].keliang<<' '<<tea[i].liuli<<' '<<tea[i].jiqing<<' '<<tea[i].qifa<<' '<<tea[i].average;
		   cout<<'\n';
		   if(tea[i].average<=100&&tea[i].average>=90)
		   {cout<<"优秀";}
		   else if(tea[i].average<90&&tea[i].average>=80)
		   {cout<<"良好";}
		   else  if(tea[i].average<80&&tea[i].average>=70)
		   {cout<<"中等";}
		   else if(tea[i].average<70&&tea[i].average>=60)
		   {cout<<"稍差";}
		   else  if(tea[i].average<60)
		   {	cout<<"差";}
	    }
	}
	if(flag==1){
		return 0;
	}
	else return 1;
}
int main()
{
	int n;char c[20];
	inputs();
	printf("请输入老师数目");
	cin>>n;
	inputt(n);
	evalu(n);
	zui(n);
	paixu(n);
	printf("请输入需要查找老师的姓名");
	cin>>c;
	while(chaxun(n,c))
		{
			printf("输入错误，请重新输入");cin>>c;
	    }

	system("pause");
	return 0;
}
