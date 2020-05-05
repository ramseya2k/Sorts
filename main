import java.io.*;
import java.util.*;
class Main 
{
  public static int[][] doubleArray = {
    {5,3,2,16},
    {9,8,10,17},
    {4,7,11,18},
    {2,5,9,12},
    {7,9,4,10}
    };
  public static void main(String[] args) 
  {
    int[][] tempArray = doubleArray; // receives original array 
    doubleArray = copyArray(tempArray); // reverts back to original array
    System.out.println("\nORIGINAL ARRAY BEFORE BUBBLE SORT IN THE 1ST COLOUMN");
    print2D(doubleArray); // prints array 
    bubbleSort(doubleArray, 4); // bubble sort in first coloumn 
    doubleArray = copyArray(tempArray); // reverts back to original array
    System.out.println("\nORIGINAL ARRAY BEFORE SELECTION SORT IN THE 2ND COLOUMN");
    print2D(doubleArray); // prints array 
    selectionSort(doubleArray, 5); // selection sort in the second coloumn 
    doubleArray = copyArray(tempArray); // reverts back to original array 
    System.out.println("\nORIGINAL ARRAY BEFORE SHELL SORT IN THE 3RD COLOUMN");
    print2D(doubleArray); // prints array 
    shellSort(doubleArray, 5); // does shell sort in the 3rd coloumn 
    doubleArray = copyArray(tempArray); // reverts back to original 
    System.out.println("\nORIGINAL ARRAY BEFORE INSERT SORT IN THE 5TH ROW");
    print2D(doubleArray); // prints array 
    insertSort(doubleArray, 4); // does insertion sort in the 5th row 
    binarySearch(doubleArray); // does binary search in 5th row and displays coloumn 
  }
  public static void bubbleSort(int[][] DA, int limit)
  {
    for(;limit>=0;limit--)
    {
      for(int index=0; index<limit; index++)
      {
        if(DA[index][0] > DA[index+1][0])
        {
          int temp = DA[index][0];
          DA[index][0] = DA[index+1][0];
          DA[index+1][0]=temp;
        }
      }
    }
    System.out.println("\nORIGINAL ARRAY AFTER BUBBLE SORT IN THE 1ST COLOUMN");
    print2D(DA);
  }
  public static void print2D(int mat[][]) // prints array 
  {  
    for (int[] row : mat){System.out.println(Arrays.toString(row));}
  } 
  public static void selectionSort(int [][] DA, int limit)
  {
    for(int i=0; i<limit;i++)
    {
      int smallest_index = i;
      for (int j = i+1; j < limit; j++)
      {
        if (DA[j][1] > DA[smallest_index][1])
        {
          smallest_index=j;
        } 
      }
      int temp = DA[smallest_index][1];
      DA[smallest_index][1] = DA[i][1]; 
      DA[i][1] = temp; 
    }
    System.out.println("\nORIGINAL ARRAY AFTER SELECTION SORT IN THE 2ND COLOUMN");
    print2D(DA);
  }
  public static void shellSort(int [][] DA, int limit)
  {
    for(int gap=limit/2; gap >= 1; gap=gap/2)
    {
      for(int i=gap; i<limit; i++)
      {
        for(int j=i; j>=gap && DA[j-gap][2]>DA[j][2]; j=j-gap)
        {
          int temp = DA[j-gap][2];
          DA[j-gap][2] = DA[j][2];
          DA[j][2] = temp;
        }
      }
    }
    System.out.println("\nORIGINAL ARRAY AFTER SHELL SORT IN THE 3RD COLOUMN");
    print2D(DA);
  }
  public static void insertSort(int [][] DA, int limit)
  {
    for(int i=1; i < limit ; i++)
    {
      for(int j=i; j>0 && DA[limit][j] < DA[limit][j-1];j--)
      {
        int temp = DA[limit][j];
        DA[limit][j] = DA[limit][j-1];
        DA[limit][j-1] = temp;
      }
    }
    System.out.println("\nORIGINAL ARRAY AFTER INSERT SORT IN THE 5TH ROW");
    print2D(DA);
  }
  public static int[][] copyArray(int[][] DA)
  {
    int[][] tempArray = new int[5][4];
    for(int row=0; row<DA.length;row++)
    {
      for(int col=0; col<DA[0].length;col++)
      {
        tempArray [row][col] = DA[row][col];
      }
    }
    return tempArray;
  }
  public static void binarySearch(int[][] DA)
  {
    Scanner input = new Scanner(System.in);
    System.out.println("\nWhat number are you looking for in the 5th row?");
    int numSearch = input.nextInt();
    int last = DA[0].length-1;
    while((last >= 0) && last < DA[4].length)
    {
      if(DA[4][last] == numSearch)
      {
        System.out.println("\nFound the number! Here is the coloumn it belongs in.\n");
        for(int i=0; i<DA.length;i++)
        {
          System.out.println(DA[i][last]);
        }
        return;
      }
      else if(DA[4][last] > numSearch)
      {
        last--;
      }
      else
      {
        last++; 
      }
    }
    System.out.println("The number you have entered was not found in the array.");
    return;
  }
}
