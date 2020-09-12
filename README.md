# strictly-increasing-decreasing-

#include<iostream>
using namespace std;

int main() 
{
	int n;
    int s;
    int error=0;
    int inc=0;
    cin>>n;
    int s1,s2;
    cin>>s1>>s2;
    if(s1>s2)
    {
    for(int i=3;i<=n;i++)
    {
        s1=s2;
        cin>>s2;
        if(s1<s2)
        {
            inc=1;
        }
        if(((inc==1)&&(s1>s2))||(s1==s2))
            error=1;
        
    }
    
    }
    else if(s1<s2)
    {
    for(int i=3;i<=n;i++)
    {
        s1=s2;
        cin>>s2;
        if(s1>s2)
        {
            inc=1;
        }
        if(((inc==1)&&(s1<s2))||s1==s2)
            error=1;
        
    }
    
    }
    else if(s1==s2)
    { 
        error=1;
        for(int i=3;i<=n;i++)
        {
            cin>>s2;
        }
    }
    
    if(error==1)
    {
        cout<<"false";
    }
    else
    {
        cout<< "true";
    }
}
