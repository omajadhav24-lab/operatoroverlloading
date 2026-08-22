#include<iostream>
using namespace std;
class op
{
    public:
    char n[20];
    
    
    friend ostream & operator <<(ostream &a,op &o1);
    friend istream & operator >>(istream &b,op &o1);
} ;
ostream & operator <<(ostream &a,op &o1)
{
    a<<"name:"<<o1.n;
} 
istream & operator >>(istream &b,op &o1)
{
    b>>o1.n;
}
int main()
{
    op obj;
    cout<<"enter your name:";
    cin>>obj;
    cout<<obj;
    return 0;

}
