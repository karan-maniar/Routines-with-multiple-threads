#include "threads.h"

int count = 1;
void f1()
{
	// int count = 1;
	while(1)
	{
		if(count > 26) count = 1;
		printf("\nf1 : %d", count++);
		yield();
	}

}

void f2()
{
	char a = 'a';
	while(1)
	{
		if(a > 'z')
			a = 'a';
		printf("\nf2 : %c", a++);
		yield();
	}
}

void f3()
{
	char ab = 'A';
	while(1)
	{
		if(ab > 'Z')
			ab = 'A';
		printf("\nf3 : %c", ab++);
		yield();
	}
}

void main()
{
	InitQ(&RunQ);
	start_thread(f1);
	start_thread(f2);
	start_thread(f3);
	run();
}
