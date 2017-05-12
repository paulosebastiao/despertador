# despertador
#include <stdio.h>
#include <stdlib.h>
#include <windows.h>


int main(){
int h = 00, m = 00, s = 00, hd, md, sd, i = 0;
char c;
printf("deseja ter alarme(s ou n)?");
scanf("%c", &c);
if(c == 's'){
printf("que horas despertara? \n");
scanf("%d %d %d", &hd, &md, &sd);
}
loop:
if (i > 0 && i <=10){
    printf("\n\a esta na hora!!!");
    Beep(1000,500);
    i ++;
}
printf("\r %.2d : %.2d : %.2d", h, m, s);
if((s == sd) && (m == md) && (h == hd))
    i ++;
s ++;
if (s > 59){
  s = 00;
  m ++;
 }
 if (m == 60){
 m = 00;
 h ++;
 }
 if (h == 24)
  h = 00;
  Sleep(1000);

  goto loop;
  return 0;
  }
