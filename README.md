
#include<iostream>
using namespace std;
#define ll long long
 void rotateInRight(int arr[], int n, int d){
    if(d>n){
        d=d%n;
    }
          int temp[n];
          int j=0;
          for(int i=n-d; i<n; i++){
            temp[j]=arr[i];
            j++;
          }
          for(int i=0; i<n-d; i++){
         temp[j]=arr[i];
         j++;
          }
          for(int i=0; i<n; i++){
           arr[i]=temp[i];
           cout << arr[i] << " ";
          }
          cout << endl;
                    
}
int main(){

    int n,d;
    // d is number of element shifting toward rights
    cin >> n >> d;
    int arr[n];
    for(int i=0; i<n;i++){
        cin >> arr[i];
    }
    rotateInRight(arr,n,d);
}
