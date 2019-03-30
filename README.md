# RCtank_2019

慶應義塾高等学校電子工学研究会　日吉祭展示用

MIT License  
Author-Kohei Wada  
oc.yaki122@gmail.com

## 注意

IRRemote と tone が Timer 関係で干渉するため、IRRemote ライブラリの "boarddefs.h" 151 行目

```c++:boarddefs.h
// ATmega48, ATmega88, ATmega168, ATmega328
	//#define IR_USE_TIMER1   // tx = pin 9
	#define IR_USE_TIMER2     // tx = pin 3
```

を

```c++:boarddefs.h
// ATmega48, ATmega88, ATmega168, ATmega328
	#define IR_USE_TIMER1   // tx = pin 9
	//#define IR_USE_TIMER2     // tx = pin 3
```

に変更する必要がある
