#include "stdafx.h"
#include <string>
#include <iostream>

using namespace std;

int main(int argc, char* argv[])
{
	int strNumA,strNumB;
	int strOperator;
	cout<<"请输入数字A：\n";
	cin>>strNumA;
	cout<<"请选择运算符号（1,+,2,-,3,*,4,/）：\n";
	cin>>strOperator;
	cout<<"请输入数字B：\n";
	cin>>strNumB;

	int strResult;
	switch(strOperator)
	{
		case OPERATOR_ADD:
			strResult = strNumA + strNumB;
			break;
		case OPERATOR_MINUS:
			strResult = strNumA - strNumB;
			break;
		case OPERATOR_MUTHL:
			strResult = strNumA * strNumB;
			break;
		case OPERATOR_DIV:
			if(strNumB!=0)
				strResult = strNumA / strNumB;
			else
				cout<<"您输入的有误，除数不能为0！"<<endl;
			break;
		default:
			cout<<"输入有错误！"<<endl;
			break;
	}
	cout<<"得到的结果是："<<strResult;
	return 0;
}
