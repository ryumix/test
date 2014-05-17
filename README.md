#include <stdio.h>
#include <stdlib.h>
#include <time.h>

void main(){
	int a, b,c,d = 0;
	int e;
	printf("ダイスを二つ振ります。出目の裏面の数字合計はいくつでしょう？\n");
	getchar();
	srand((unsigned)time(NULL));
	a = rand() % 6;
	b = rand() % 6;
	if(a==0){
		c=1;
	}
	if(a==1){
		c=2;
	}
	if(a==2){
		c=3;
	}
	if(a==3){
		c=4;
	}
	if(a==4){
		c=5;
	}
	if(a==5){
		c=6;
	}
	if(b==0){
		d=1;
	}
	if(b==1){
		d=2;
	}
	if(b==2){
		d=3;
	}
	if(b==3){
		d=4;
	}
	if(b==4){
		d=5;
	}
	if(b==5){
		d=6;
	}
			
	printf("ダイスXは%d、ダイスYは%d\n足して%d。では裏面の合計は？（回答範囲は２～１２）\n", c, d,c+d);
	
	scanf("%d",&e);
	if(e==14-(c+d)){
		if (1 > e || e<13){
			printf("正解！！サイコロ買って遊んでね！！\n");
			getchar();
		}
	}
	else if (e != 14 - (c + d)){
		if (1 > e || e < 13){
			printf("ハズレ！！サイコロ買って確認してね！！\n");
			getchar();
		}

		else {
			printf("回答範囲外！！サイコロ買ってから出直してこい！！\n");
			getchar();
		}
	}
	getchar();
}
