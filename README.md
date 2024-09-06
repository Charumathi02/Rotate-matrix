static void rotate90Clockwise(int a[][])
{
int N= a.length ;
	for (int i = 0; i < N / 2; i++)
	{
		for (int j = i; j <  N  - i - 1; j++)
		{
			int temp = a[i][j];
			a[i][j] = a[N - 1 - j][i];
			a[N - 1 - j][i] = a[N - 1 - i][N - 1 - j];
			a[N - 1 - i][N - 1 - j] = a[j][N - 1 - i];
			a[j][N - 1 - i] = temp;
		}
	}
}
static void printMatrix(int arr[][])
{ 
    System.out.println("Rotated matrix");
	for (int i = 0; i <  arr.length ; i++)
	{
		for (int j = 0; j <arr.length ; j++)
		System.out.print( arr[i][j] + " ");
		System.out.println();
	}
}
