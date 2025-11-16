# SERIAL-TRANSFER-OF-SINGLE-BYTE-CHARACTER-USING-8051-KEIL.-EMBEDDED-C-PROGRAM-

**AIM:** 

To write and execute Embedded C Program for Serial Transfer of Single Byte / Character using 8051 KEIL

**APPARATUS REQUIRED:**

Personal computer with Keil software

**PROGRAM:**

**(i)	Serial port transfer a character A**

#include<reg51.h> void main(void)

{

TMOD=0X20;//TIMER 1,MODE 2 TH1=0XFA;

SCON=0X50; TR1=1;

while(1)

{ SBUF='A';

while(TI==0); TI=0;

}

}

**(ii)	Serial port to Transfer a Message**

#include<reg51.h> void main(void)

{

unsigned char msg[]="Programming 8051"; unsigned char i;

TMOD=0X20;//TIMER 1,MODE 2 TH1=0XFA;

SCON=0X50; TR1=1;

for (i=0; i<17;i++)

{

SBUF= msg[i]; while(TI==0); TI=0;

}

while(1);

}

 
**OUTPUT:**
<img width="1919" height="1151" alt="505803094-55070cc5-c877-4638-85ad-aa36442528ca" src="https://github.com/user-attachments/assets/e4affc3c-b5be-421f-b7d1-01d458d4f1d6" />
<img width="2879" height="1706" alt="511805540-7311d649-bc94-4f8d-9f5e-6e4d94fac7f1" src="https://github.com/user-attachments/assets/93ff9e04-603f-41aa-bedf-3facdc13c389" />


<br>
<br>
<br>
<br>
<br>

**Result:**

Thus the Serial transfer of Single Byte / Character using 8051 KEIL was done and shown the output.
