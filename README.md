# prime-numbers-sum
sum of all prime numbers within a positive sequence


#include <iostream>
using namespace std;

int main(){

    int x , y , sum = 0 , isPrime;
    cout << "Enter the left range x: ";
    cin >> x;
    cout << "Enter the right range y: ";
    cin >> y;
    

    for(int i=x; i<=y; i++){
        if(i==0 || i==1){
            continue;
        }
        isPrime = 1;
        for(int j = 2; j<=i/2; j++){
            if(i%j==0){
                isPrime = 0;
                break;
            }
        }
        if(isPrime==1){
            if(i!=0){
                cout << i << " + ";
                sum += i;
            }

        }


    }
    cout << " = " << sum;

    return 0;
}
