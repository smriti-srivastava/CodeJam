int hourglassSum(int arr_rows, int arr_columns, int** arr) 
{
    int row_index, column_index, hoursum = 0, maximum_sum = -999;
    for(row_index = 1; row_index < arr_rows-1; row_index++)
    {
        for(column_index = 1; column_index < arr_columns-1; column_index++)
        {
            hoursum = arr[row_index][column_index] + arr[row_index-1][column_index] + arr[row_index+1][column_index] + arr[row_index-1][column_index-1] + arr[row_index-1][column_index+1] +  arr[row_index+1][column_index-1] + arr[row_index+1][column_index+1];
           if(maximum_sum < hoursum)
                maximum_sum = hoursum;
        }
    }
    return maximum_sum;

}
