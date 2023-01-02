# Random_Password_Generator_C++


#include <stdio.h>
#include <iostream>
#include <ctime>
using namespace std;

 const char cAlphaNumSpec [] = "1234567890!@#$%^&*abcdefghijklmnopqrstuvwxyzABCDEFGHIJKLMNOPQRSTUVWXYZ";
 const char alphaNumSpec [] = "1234567890!@#$%^&*abcdefghijklmnopqrstuvwxyz";
 const char cAlphaNum [] = "1234567890abcdefghijklmnopqrstuvwxyzABCDEFGHIJKLMNOPQRSTUVWXYZ";   
 const char alphaNum [] = "1234567890abcdefghijklmnopqrstuvwxyz";

//  int string_length = sizeof(alphaNumSpec);

int main()
{
   int length = 0;
   char capLetters;
   char specChar;
    
    cout<<"RANDOM PASSWORD GENERATOR"<<endl;
    cout<<"*************************"<<endl;
    cout<<"Enter length  of password: "<<endl;
    cin>>length;
    cout<<"Should it include capital letters? (Y/N)"<<endl;
    cin>>capLetters;
    cout<< "Should it include special characters?(Y/N)"<<endl;
    cin>> specChar;
    
    srand(time(0));
    
    if(capLetters == 'Y'||'y' && specChar == 'Y'||'y'){
        
        int string_length = sizeof(cAlphaNumSpec);
         cout<<" Here is your random generated password: "<<endl;
    
        for(int  i = 0; i<length;i++){
        cout<< cAlphaNumSpec[rand() % string_length];
        
        }
    
    } else if(capLetters == 'Y'||'y' && specChar == 'N'||'n'){
        
         int string_length = sizeof(cAlphaNum);
         cout<<" Here is your random generated password: "<<endl;
    
        for(int  i = 0; i<length;i++){
        cout<< cAlphaNum[rand() % string_length];
        
        
         }
    } else if ( capLetters == 'N'||'n' && specChar == 'Y'||'y'){
        
        int string_length = sizeof(alphaNumSpec);
         cout<<" Here is your random generated password: "<<endl;
    
        for(int  i = 0; i<length;i++){
        cout<< alphaNumSpec[rand() % string_length];
        
        
        }
    } else {
         int string_length = sizeof(alphaNum);
         cout<<" Here is your random generated password: "<<endl;
    
        for(int  i = 0; i<length;i++){
        cout<< alphaNum[rand() % string_length];
        
         }
    }
    
 
    return 0;

}
