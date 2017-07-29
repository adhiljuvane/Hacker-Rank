# Hacker-Rank
Hackerrank/Algorithms/Implimentation/Cut the sticks.

this is my solution for the above problem in Hackerrank.

**********************************************************************

#include <cmath>
#include <cstdio>
#include <vector>
#include <iostream>
#include <algorithm>
using namespace std;

int main(){
    int n,i,k,count;
    cin >> n;
    vector<int> arr(n);
    for(int arr_i = 0;arr_i < n;arr_i++){
       cin >> arr[arr_i];
    }
   // cout<<n<<endl;
    count=n;
    while(count>0)
    {
        cout<<count<<endl;
        k=1000;
    for(i=0;i<n;i++)
    {
        if(arr[i]<k && arr[i]>0 )
            k=arr[i];
    }
        count=0;
        for(i=0;i<n;i++)
        {
            arr[i]=arr[i]-k;
            if(arr[i]>0)
                count++;
        }
    }
    
    return 0;
}

*************************************************************
