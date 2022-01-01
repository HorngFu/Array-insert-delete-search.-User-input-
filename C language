#include <stdio.h>
//DSA homework1: Array: insert, delete, search.
void show_element(int n, int array[n]);
void insert_element(int n, int array[n]);
void delete_element(int n, int array[n]);
void search_element(int n, int array[n]);

int main(){
	int choise;
	int array_number[10],i,size;

   printf("enter each elements :\n");
   
   for(i=0;i<10;i++)
      scanf("%d",&array_number[i]);  //select option
	printf("Options\n   1.Show elements of array\n   2.Insert an element to array\n\
   3.Delete an element\n   4.Search element\n ======================>>> Option ");
    scanf("%d", &choise);
    
	if (choise == 1){
		show_element(10, array_number);
	}else if(choise == 2){
		insert_element(10, array_number);
	}else if(choise == 3){
		delete_element(10, array_number);
	}else if(choise == 4){
		search_element(10, array_number);
	}else{
		printf("No Option.");
	}
	return 0;
}

void show_element(int n, int array_number[])  //show element function
{
	int i;
	for(i = 0; i < n; i++){
		printf("%d ", array_number[i]);
	}
}
void insert_element(int n, int array_number[]){  //insert element fuction
	int i,j,k,l;
	
	printf("Insert index number: ");
	scanf("%d", &i);
	
	printf("insert number to new %dindex's: ", i);
	scanf("%d", &j);
	
	printf("Before insert: \n");
	show_element(9, array_number);
	printf("After insert: ");
	
	for(k = 0; k < n; k++){
		if(k == i){
			for(l = 0; l < n - k; l++){
				array_number[n - l] =array_number[n - l - 1];
			}
		array_number[k] = j;
		}
	}
	for(k = 0; k < n; k++){
		printf("%d ", array_number[k]);
	}
}
void delete_element(int n, int array_number[n])    //delete element function
{
	int i,j,k;
	printf("Which index you want to delete? \n");
	scanf("%d", &i);
	
	printf("Before: ");
	show_element(10, array_number);
	
	printf("\nAfter deleted: ");
	for(j = 0; j < n; j++){
		if(j == i){
			for(k = j; k < n; k++){
				array_number[k] = array_number[k + 1];
			}
		}
	}
	array_number[9] = 0;
	
	for(k = 0; k < n ; k++){
		printf("%d ", array_number[k]);
	}
}
void search_element(int n, int array_number[n]){   //search element function
	int i,j,k,count = 0;
	
	printf("Options:\n1.Non-duplicate\n2.Duplicate\n");
	scanf("%d", &i);
	
	if(i == 1){
		printf("1.Non-duplicate\n");			//non_duplicate
		printf("Elements of array: ");
		show_element(10, array_number);
		puts("");
		printf("What's the number you want to search? ");
		scanf("%d", &j);
		for(k = 0; k < n; k++){
			if(array_number[k] == j){
				count = 1;
				break;
			}
		}
		
		if(count == 0)
			printf("Not found.");
		else
			printf("Found in index %d", k);
	}else if(i == 2){
		printf("2.Duplicate\n");        //duplicate
		printf("Elements of array: ");
		show_element(10, array_number);
		puts("");
		printf("What's the number you want to search?");
		scanf("%d", &j);
		for(k = 0; k < n; k++){
			if(array_number[k] == j){
				count++;
				printf("Search found at index: %d\n", k);
			}
		}
		if(count == 0){
			printf("Not found.");
		}
	}
}

