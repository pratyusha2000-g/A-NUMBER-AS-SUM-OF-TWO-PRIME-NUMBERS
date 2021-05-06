# A-NUMBER-AS-SUM-OF-TWO-PRIME-NUMBERS
#include <iostream>
int prime(int n);
using namespace std;
int main()
{
    int n,i,p,s;

    cout<< "Enter the number "<<endl;
    cin>>n;
    
    for ( i = 1; i<= n/2; ++i)
    {
        p= prime(i);
        if(p==1)
        {
            s=prime(n-i);
            if(s==1)
            cout<<n<<"="<<i<<"+"<<n-i<<" ";
        }
    }
    


        return 0;
}    

int prime(int n)
{
    int i,c=0;
    for(i=2;i<=n/2;i++)
       if(n%i==0)
          c++;
        
    if(c==0)
    return 1;
    else
    return 0;
}    
