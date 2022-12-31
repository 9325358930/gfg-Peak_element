# gfg-Peak_element
problem solving

Example 1:

Input: 
N = 3
arr[] = {1,2,3}
Possible Answer: 2
Generated Output: 1
Explanation: index 2 is 3.
It is the peak element as it is 
greater than its neighbour 2.
If 2 is returned then the generated output will be 1 else 0.


class Solution
{
    public:
    int peakElement(int arr[], int n)
    {
       int low=0;
       int high=n-1;
       int mid=low+(high-low)/2;

       while(low<high){
           if(arr[mid]>=arr[mid+1] && arr[mid]>arr[mid-1]){
               return mid;
           }
           if(arr[mid]<arr[mid+1]){
               low=mid+1;
           }
           else{
               high=mid-1;
           }
           mid=low+(high-low)/2;
       }
       return mid;
    }
};
