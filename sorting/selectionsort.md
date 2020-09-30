# Selection Sort
Selection sort is an in-place comparison sorting algorithm. This algorithm sorts an array by repeatedly finding the minimum element from unsorted part and putting it at the beginning. The algorithm maintains two subarrays in a given array.
1) The subarray which is already sorted.
2) Remaining subarray which is unsorted.
In every iteration of selection sort, the minimum element (considering ascending order) from the unsorted subarray is picked and moved to the sorted subarray.

## Sample Code
```cpp
# include  < iostream >
# include  < algorithm >

using  namespace  std ;

void  selectionSort ( int arr[], int n){

    for ( int i = 0 ; i <n; i ++){
        // Find the minimum value in the interval (i, n)
        int minIndex = i;
        for ( int j = i + 1 ; j <n; j ++)
            if (arr[j] <arr[minIndex])
                minIndex = j;

        swap (arr[i], arr[minIndex] );
    }

}

int  main () {

    int a[ 10 ] = { 10 , 9 , 8 , 7 , 6 , 5 , 4 , 3 , 2 , 1 };
    selectionSort (a, 10 );
    for ( int i = 0 ; i < 10 ; i ++)
        cout<<a[i]<< "  " ;
    cout<<endl;

    return  0 ;
}
```	

## Space Complexity: O(1)

## Time Complexity
| Best          | Average     | Worst |
| --------------|:-----------:| -----:|
| O(N^2) | O(N^2) | O(N^2)|

* [Animated Selection Sort Display](https://www.toptal.com/developers/sorting-algorithms/selection-sort)
