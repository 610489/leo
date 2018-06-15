

# C程式編譯組譯與逆向(反編譯)
# C語言程式編譯與組譯
```
#include <stdio.h>

int main()
{
   printf("Hello CTFer\n ”);
   return 0;
}
```
【推薦好書】程式設計師的自我修養：連結、載入、程式

## 預處理階段
```

gcc –E XXX.c –o XXX.i (查看XXX.i的架構)
#編譯階段
gcc –S XXX.i  –o XXX.s(查看XXX.s的架構)
```
## 組譯階段

gcc –c XXX.s –o XXX.o(查看XXX.o的架構)
```
 1 "helloCTFer.c"
 1 "<built-in>"
 1 "<command-line>"
 31 "<command-line>"
 1 "/usr/include/stdc-predef.h" 1 3 4
 32 "<command-line>" 2
 1 "helloCTFer.c"
 1 "/usr/include/stdio.h" 1 3 4
 27 "/usr/include/stdio.h" 3 4
 1 "/usr/include/features.h" 1 3 4
 364 "/usr/include/features.h" 3 4
 1 "/usr/include/i386-linux-gnu/sys/cdefs.h" 1 3 4
 415 "/usr/include/i386-linux-gnu/sys/cdefs.h" 3 4
 1 "/usr/include/i386-linux-gnu/bits/wordsize.h" 1 3 4
 416 "/usr/include/i386-linux-gnu/sys/cdefs.h" 2 3 4
 365 "/usr/include/features.h" 2 3 4
 388 "/usr/include/features.h" 3 4
 1 "/usr/include/i386-linux-gnu/gnu/stubs.h" 1 3 4

 1 "/usr/include/i386-linux-gnu/gnu/stubs-32.h" 1 3 4
 8 "/usr/include/i386-linux-gnu/gnu/stubs.h" 2 3 4
 389 "/usr/include/features.h" 2 3 4
 28 "/usr/include/stdio.h" 2 3 4
……………………………….

```


## 連結階段
gcc  XXX.o –o XXX(產生的可執行檔)

















## 組譯過程
```
 1 "helloCTFer.c"
 1 "<built-in>"
 1 "<command-line>"
 31 "<command-line>"
 1 "/usr/include/stdc-predef.h" 1 3 4
 32 "<command-line>" 2
 1 "helloCTFer.c"
 1 "/usr/include/stdio.h" 1 3 4
 27 "/usr/include/stdio.h" 3 4
 1 "/usr/include/features.h" 1 3 4
 364 "/usr/include/features.h" 3 4
 1 "/usr/include/i386-linux-gnu/sys/cdefs.h" 1 3 4
 415 "/usr/include/i386-linux-gnu/sys/cdefs.h" 3 4
 1 "/usr/include/i386-linux-gnu/bits/wordsize.h" 1 3 4
 416 "/usr/include/i386-linux-gnu/sys/cdefs.h" 2 3 4
 365 "/usr/include/features.h" 2 3 4
 388 "/usr/include/features.h" 3 4
 1 "/usr/include/i386-linux-gnu/gnu/stubs.h" 1 3 4

 1 "/usr/include/i386-linux-gnu/gnu/stubs-32.h" 1 3 4
 8 "/usr/include/i386-linux-gnu/gnu/stubs.h" 2 3 4
 389 "/usr/include/features.h" 2 3 4
 28 "/usr/include/stdio.h" 2 3 4
……………………………….
```
#將組合語言程式碼轉成機器可以執行的指令(instructions)
#每一個組語語句都對應一機器指令。
#組譯器的組譯過程相對於編譯器來講比較簡單
#沒有複雜的語法，也沒有語意，也不需要做指令最佳化，只是根據組語指令和機器指令的對照表一一翻譯就可以
#連結過程
