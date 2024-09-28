# Frame-by-frame-typing
逐帧打字术

**仅支持C++语言**

```cpp
// Suggest not to change the code randomly.
// This program only supports output of uppercase and lowercase letters and spaces 
// User Customize
#define outstr "Hello World" //Change the output string.
#define wait 1 //Set the wait time, 0 if no wait. 





//Code 
#include <iostream>
#include<cstdlib>
#include <string>
#include<ctime>
#include <windows.h>
using namespace std;
const string s=outstr;
char fun(void)
{
	int rd=rand()%53;
	if (rd==52)
		return ' ';
	if (rd>=0 and rd<=25)
		return rd+'A';
	else
		return rd-26+'a';
}
int main()
{
	
	srand(time(0));
	for (int i=0;i<s.size();i++)
	{
		int o;
		do
		{
			o=fun();
			for (int j=0;j<i;j++)
				printf("%c",s[j]);
			printf("%c\n",o);
			Sleep(wait);
		} while (o!=s[i]);
		
	}
	return 0;
}
```
