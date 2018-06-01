
## c語言程式編譯組譯與與逆向
- c語言程式編譯組譯
```
#include <stdio.h>

int x=5;

int main()
{
   printf("Hello CTFer\n ”);
   return 0;
}
```
![image](https://github.com/wutizhi/CTF/blob/master/photo/Screenshot%20from%202018-06-01%2009-03-35.png)
- 步驟1:預處理階段\
```
gcc –E XXX.c –o XXX.i \
```
查看.i的架構==>hello.i \
- 步驟2:編譯階段:產生組語\
```
gcc –S XXX.i  –o XXX.s
```
查看.s的架構==>hello.s \

![image](https://github.com/wutizhi/CTF/blob/master/photo/Screenshot%20from%202018-06-01%2009-12-07.png)
![image](https://github.com/wutizhi/CTF/blob/master/photo/Screenshot%20from%202018-06-01%2009-12-26.png)
![image](https://github.com/wutizhi/CTF/blob/master/photo/Screenshot%20from%202018-06-01%2009-13-27.png)
![image](https://github.com/wutizhi/CTF/blob/master/photo/Screenshot%20from%202018-06-01%2009-14-18.png)
