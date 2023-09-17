#Advanced 
\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_
|\_\_\_\_|\_\_\_\_|\_\_\_\_|\_\_\_\_|
|\_\_\_\_|\_\_\_\_|\_\_\_\_|
|\_\_\_\_|\_\_\_\_|

int\[]\[] matrix = new int\[3]\[];
	matrix\[0]=new int\[3];
		matrix\[0]\[0] = 1;
		matrix\[0]\[1] = 2;
		matrix\[0]\[2] = 3;
	matrix\[1]=new int\[2]
		matrix\[1]\[0] = 4;
		matrix\[1]\[1] = 5;
	matrix\[2]=new int\[1];
		matrix\[2]\[0]=6;
ВСЕКИ МАСИВ (РЕД) МОЖЕ ДА БЪДЕ С РАЗЛИЧНА ДЪЛЖИНА!

int\[] example = matrix\[2]; //нормален масив
for(int row=0; row<matrix.Lenght; row++){
	for(int col=0; col<matrix\[row].Lenght; col++){
		Console.Write(matrix\[row]\[col]+" ");
	}   
	Console.ReadLine();
}   //обхождане на назъбен масив

[[Multidimensional Arrays МАТРИЦИ]]