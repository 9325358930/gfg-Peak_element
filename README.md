# gfg-Peak_element
problem solving























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
