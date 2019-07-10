# C_Class_190710
1

#include <stdio.h>
void main()
{
	// char H[] = { '0','1','2','3','4','5','6','7','8','9','A','B','C','D','E','F' };
	char H[16];
	int x[20];
	int d, m, n, c = 0, i, dd;
	for (i = 0; i <= 9; i++) H[i] = char(48 + i);
	for (i = 10; i <= 15; i++) H[i] = char(55 + i);
	printf("진법 변환 할 10진수를 입력하시오.\n");  // 유도인쇄
	scanf_s("%d", &d);
	dd = d;
	do
	{
		m = d / 16;
		n = d % 16;
		c++;
		x[c] = n;
		d = m;
	} while (m != 0);
	for (i = c; i >= 1; i--)
	{
		/*
		if (x[i] == 10) printf("A");
		else if (x[i] == 11) printf("B");
		else if (x[i] == 12) printf("C");
		else if (x[i] == 13) printf("D");
		else if (x[i] == 14) printf("E");
		else if (x[i] == 15) printf("F");
		else printf("%d", x[i]);
		*/
		printf("%c", H[x[i]]);
	}
	printf("(16) \n");
	d = dd;
	c = 0;
	do
	{
		m = d / 8;
		n = d % 8;
		c++;
		x[c] = n;
		d = m;
	} while (m != 0);
	for (i = c; i >= 1; i--)
		printf("%c", H[x[i]]);
	printf("(8) \n");
	d = dd;
	c = 0;
	do
	{
		m = d / 2;
		n = d % 2;
		c++;
		x[c] = n;
		d = m;
	} while (m != 0);
	for (i = c; i >= 1; i--)
		printf("%c", H[x[i]]);
	printf("(2) \n");
}


/*
if (x[i] == 10) printf("A");
else if (x[i] == 11) printf("B");
else if (x[i] == 12) printf("C");
else if (x[i] == 13) printf("D");
else if (x[i] == 14) printf("E");
else if (x[i] == 15) printf("F");
printf("%d", x[i]);	

printf("%c", H[x[i]]);
한 줄로 간략히 축소됨
*/
