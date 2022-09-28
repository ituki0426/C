
# スタック

スタックにデータを積む関数pushとデータを取り出す関数popを作る。

データを棚（stack）の下部から順に積んでいき、必要に応じて上部から取り出していく方式（後入れ先出し）のデータ構造をスタックという。

スタックは1次元配列を用いて実現できる。

![image](https://user-images.githubusercontent.com/82156802/192754414-aa99557f-c6dd-478b-b243-687f037ec42f.png)

![image](https://user-images.githubusercontent.com/82156802/192759265-c69f18d9-a9b0-4f2d-a2f7-38537662b457.png)

![image](https://user-images.githubusercontent.com/82156802/192759298-36a371a5-1d62-41e4-b658-fc174e7baab5.png)


```c
#include <stdio.h>

#define MaxSize 100
int stack[MaxSize];
int sp= 0;
int push(int);
int pop(int *);

int main(void){
	int c,n;
	while(printf("]"),(c=getchar())!=EOF){
		rewind(stdin);
		if(c=='i' || c=='I'){
			printf("data---> ");
			scanf("%d",&n); rewind(stdin);
			if(push(n)==-1){
				printf("スタックがいっぱいです");
			}
		}
		if(c=='o' || c=='O'){
			if(pop(&n)==-1){
				printf("スタックがいっぱいです");
			}
			else{
				printf("stack data ---> %d",n);
			}
		}
	}
}
int push(int n){
	if(sp<MaxSize){
		stack[sp++]=n;
		return 0;
	}else{
		return -1;
	}
}
int pop(int *n){
	if(sp>0){
		*n = stack[--sp];
	}else{
		return -1;
	}
}
```
