# Codeforcescpp-208A
#include <bits/stdc++.h>

using namespace std;

int main(){
  string s;
  cin >> s;
  int len = s.length();

  //flag variable eleminates multiple spacing between the words
  int flag = 1;

  //tmp variable removes spaces at the begining
  int tmp = 1;
  
  for(int i=0;i<len;i++){

    if(s.substr(i,3)=="WUB"){
      if(tmp==1){
        i+=2;
      }
      else{
        i+=2;
        if(flag==1){
          cout << " ";
        }
        flag = 0;
      }
    }
    else{
      tmp = 0;
      cout << s[i];
      flag = 1;
    }
  }
  return 0;
}
