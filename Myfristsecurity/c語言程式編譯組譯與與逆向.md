
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
- 步驟1:預處理階段
```
gcc –E XXX.c –o XXX.i 
```
查看.i的架構==>hello.i 
https://github.com/wutizhi/CTF/blob/master/Myfristsecurity/hello.i
- 步驟2:編譯階段:產生組語
```
gcc –S XXX.i  –o XXX.s
```
查看.s的架構==>hello.s 
https://github.com/wutizhi/CTF/blob/master/Myfristsecurity/hello.s

![image](https://github.com/wutizhi/CTF/blob/master/photo/Screenshot%20from%202018-06-01%2009-12-07.png)
![image](https://github.com/wutizhi/CTF/blob/master/photo/Screenshot%20from%202018-06-01%2009-12-26.png)
- 步驟3:組譯過程
```
gcc –c XXX.s –o XXX.o
```
使用xxd看看onject file的內容==>xxd hello.o
```
00000000: 7f45 4c46 0201 0100 0000 0000 0000 0000  .ELF............
00000010: 0100 3e00 0100 0000 0000 0000 0000 0000  ..>.............
00000020: 0000 0000 0000 0000 a002 0000 0000 0000  ................
00000030: 0000 0000 4000 0000 0000 4000 0d00 0a00  ....@.....@.....
00000040: 5548 89e5 bf00 0000 00e8 0000 0000 b800  UH..............
00000050: 0000 005d c348 656c 6c6f 2043 5446 6572  ...].Hello CTFer
00000060: 0000 4743 433a 2028 5562 756e 7475 2035  ..GCC: (Ubuntu 5
00000070: 2e34 2e30 2d36 7562 756e 7475 317e 3136  .4.0-6ubuntu1~16
00000080: 2e30 342e 3529 2035 2e34 2e30 2032 3031  .04.5) 5.4.0 201
00000090: 3630 3630 3900 0000 1400 0000 0000 0000  60609...........
000000a0: 017a 5200 0178 1001 1b0c 0708 9001 0000  .zR..x..........
000000b0: 1c00 0000 1c00 0000 0000 0000 1500 0000  ................
000000c0: 0041 0e10 8602 430d 0650 0c07 0800 0000  .A....C..P......
000000d0: 0000 0000 0000 0000 0000 0000 0000 0000  ................
000000e0: 0000 0000 0000 0000 0100 0000 0400 f1ff  ................
000000f0: 0000 0000 0000 0000 0000 0000 0000 0000  ................

```
![image](https://github.com/wutizhi/CTF/blob/master/photo/Screenshot%20from%202018-06-01%2009-13-27.png)
- 步驟4:連結階段
```
gcc XXX.o -o XXX
```
產生可執行檔
```
strings XXX
```
![image](https://github.com/wutizhi/CTF/blob/master/photo/Screenshot%20from%202018-06-01%2009-14-18.png)
