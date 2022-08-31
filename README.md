# Program_Study

# 8월 31일

// byte(1바이트 0 ~ 255), short(2바이트 -3만~3만), int(4바이트 -21억~21억), long(8바이트)
// sbyte(1바이트 -128~127), ushort(2바이트 0~6만) unit(4바이트, 0~43억), ulong(8바이트)

int hp;
short level = 100;
long id;

// 게임서버에서 id 갯수 같은 경우에는 나중에 21억이 넘어가긴함.이런경우 long을 쓰겠지?
hp = 100;

byte attack = 0;
attack--;

Console.WriteLine("Hello Number ! {0}", attack);


// 10진수
// 00 01 02 03 04 05 06 07 08 09 10

// 2진수 (0b)
// 0b00 0b01 0b10 0b11 0b100
// 0b10001111 = 0x8F  (4개씩 끊어서 읽음)

// 16진수 (0x)
// 0~9 a b c d e f  (15까지)
// 0x00 0x01 0x02 ... 0x0F
// 0x10

//0b11111111 = 255

//최상위 비트는 음수
0000 0000
-128 64 32 16 8 4 2 1

ex) 0110 0110  = 102
-102로 만드려면
1) 숫자 뒤집어 주고 (1001 1001)
2) 1만큼 더해줌
1001 1010 = -102


// bool
					bool b;

					b = true;
					b = false;

// 4바이트
					float f = 3.14f;
// 8바이트
					double d = 3.14;

// 2바이트
					char c = '가';
					string str = "Hello";

					Console.WriteLine(str);

// 1. 바구니 크기가 다른 경우
            int a = 0x0FFFFFFF;
            short b = (short)a;
            // short가 2바이트니까 0xFFFF까지만 저장이 됨 (-1)
            
            // 2. 바구니 크기는 같긴 한데, 부호가 다른 경우
            byte c = 255;
            sbyte sb = (sbyte)c;
            //underflow, overflow
            //0xFF = 0b11111111 = -1
            
            //3. 소수
            float f = 3.1414f;
            double d = f;
            
            // f를 d로 불러와도 완전히 동일한 값이 나오진 않음. 유사한 값이 불려옴 3.14141109같은
