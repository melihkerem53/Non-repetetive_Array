#include <stdio.h>

#define BOYUT (sizeof(Tekrarli) / sizeof(Tekrarli[0]))

int main()
{
	int Tekrarli[] = { 1,2,3,3,5,4,3,3,3,3,3,3,3,3,3,4,5,7,8,9,0 };
	int Tekrarsiz[BOYUT];

	int say = 0;
	for (int i = 0; i < BOYUT; i++)
	{
		int benzersiz = 1;

		for (int j = 0; j < i; j++)
		{
			if (Tekrarli[i] == Tekrarli[j])
			{
				benzersiz = 0;
				break;
			}
		}

		if (benzersiz == 1)
		{
			Tekrarsiz[say] = Tekrarli[i];
			say++;
		}
	}

	for (int i = 0; i < say; i++)
	{
		printf("%d\n", Tekrarsiz[i]);
	}

	return 0;
}
