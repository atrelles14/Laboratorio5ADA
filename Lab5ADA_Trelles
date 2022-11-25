#include <stdlib.h>
#include <stdio.h>
#define MAX 25
 
 void intercambio(int arr[],int i, int j, int ref);
 void quicksort(int arr[],int inf, int sup, int ref); 
 void ImpresionArr(int arr[],int elem);
 
 int main()
 {
 int arr[MAX]={0};
 int numElem,i;
 
 printf("De cuántos elementos será su arreglo? :  ");
 scanf("%d",&numElem);
 	for(i=0;i<numElem;i++){ 
 		printf("Elemento %d: ",i+1);
 		scanf("%d",&arr[i]);
 	}
 printf("\nArreglo sin el ordenamiento: \n");
		for (int i = 0; i < numElem; i++) {
		printf("[%d]", arr[i]);
		}
 quicksort(arr,0,numElem-1, numElem);
 ImpresionArr(arr,numElem);
 
 return 0;
 }
 
 void intercambio(int arr[],int i, int j, int ref)
 {
 int pre;
 pre=arr[i];
 printf("\n[%d] intercambia posicion con [%d]", pre, arr[j]);
 arr[i]=arr[j];
 arr[j]=pre;

printf("\nIntercambio en el Arreglo:");
	for(int i=0; i<ref; i++){
	printf("[%d] ", arr[i]);
}
printf("\n");
 }
 
 
 void quicksort(int arr[],int inf, int sup, int ref)
 {
 int i,j,x;
 i=inf;
 j=sup;
 x=arr[(i+j)/2]; //obteniendo el pivote
 
 printf("\nNuestro pivote sera: %d",x);
 
 while(i<=j)
 { 
 	while(arr[i]<x)    //elemento mayor a la izq. del pivote
 	i++;
 	while(arr[j]>x)   // elemento mayor a la der. del pivote
 	j--;
 	if(i<=j)            
 		{
 		intercambio(arr,i,j, ref);     //intercambio hasta que se cumplan condicionales
 		i++;
 		j--;
		}

 }
 if(inf<j)
 quicksort(arr,inf,j, ref);
 if(i<sup)
 quicksort(arr,i,sup, ref);
 }
 
 void ImpresionArr(int arr[],int elem)
 {
 int i;
 printf("\nSu arreglo final ordenado por el metodo de quicksort es :\n");
 	for(i=0;i<elem;i++)
 {
 printf("[%d] ",arr[i]);
 }
 }
