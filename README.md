//# Array-element-shift-by-n-digit
#include<iostream>
using namespace std;
int main(){
    int a[5] = {10,20,30,40,50};
    int temp[5];
    int n=5;
    int shiftgiven=21;
    int i,j=0;
    int shift = shiftgiven%n;
    for(i=n-shift;i<n;i++){
        temp[j] = a[i];
        j++;
    }
    for(i=n-shift-1;i>=0;i--){
        a[i+shift] = a[i];
    }
    for(i=0;i<shift;i++){
        a[i] = temp[i];
    }
    for(i=0;i<n;i++){
        cout<<a[i]<<" ";
    }
    return 0;
}
