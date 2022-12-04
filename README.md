# recursive-asal-sayi-bulma
#include<stdio.h>
int asalSayi(int,int);

int main(void)
{
	int sayi,sonuc;
	printf("lütfen bir sayi giriniz");
	scanf("%d",&sayi);
	sonuc=asalSayi(sayi,sayi/2);
	if(sonuc==0)
	{
		printf("girilen %d sayisi asal degildir\n",sayi);
	}
	else
	{
		printf("girilen %d sayisi asal sayidir\n",sayi);
	}
	return 0;
}

int asalSayi(int x,int i)
{
	if(x<2)
	return 0;
	else if(i==1)
	return 1;
	else if(x%i==0)
	return 0;
	return asalSayi(x,i-1);
}
