# code.1111
Find element occuring once when all other are present thrice
//User function Template for C++

class Solution {
  public:
    int singleElement(int arr[] ,int N) {
        // code here
        sort(arr,arr+N);
        int ans=0;
        for(int i=1;i<N-1;i++){
            if(arr[i]!=arr[i-1]&&arr[i+1]!=arr[i]){
                ans=arr[i];
            }
        }
        if(arr[N-1]!=arr[N-2]){
            ans=arr[N-1];
        }
        else if(arr[0]!=arr[1]){
            ans=arr[0];
        }
        return ans;
    }
};
