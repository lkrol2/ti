# JP

ZAJECIA 1

```c
#include <stdio.h>
int main(){
 int a,b;
 a=3;
 b=7;
 printf ("%d*%d=%d\n", a,b, a*b);
 printf ("%d/%d=%d\n", a,b, a/b);
 printf ("%d+%d=%d\n", a,b, a+b);
 printf ("%d-%d=%d\n", a,b, a-b);
 getchar();
 return 0;
}
```
będzie błąd przy mnożeniu

```c
#include <stdio.h>
int main(){
 double a,b;
 a=3;
 b=7;
 printf ("%lf*%lf=%lf\n", a,b, a*b);
 printf ("%lf/%lf=%lf\n", a,b, a/b);
 printf ("%lf+%lf=%lf\n", a,b, a+b);
 printf ("%lf-%lf=%lf\n", a,b, a-b);
 getchar();
 return 0;
}
```
pokaże wszystkie jako np. 21.000000

```c
#include <stdio.h>
int main(){
 double a,b;
 a=3;
 b=7;
 printf ("%.0lf*%.0lf=%.0lf\n", a,b, a*b);
 printf ("%lf/%lf=%lf\n", a,b, a/b);
 printf ("%.0lf+%.0lf=%.0lf\n", a,b, a+b);
 printf ("%.0lf-%.0lf=%.0lf\n", a,b, a-b);
 getchar();
 return 0;
}
```
pokaże sumę, różnicę, iloczyn jako całkowite /zmiennoprzecinkowe ale z zero miejsc po przecinku, a dzielenie z miejscami po przecinku.

```c
#include <stdio.h>
#include <math.h>
int main(){
 double r;
 int a;
 a=2;
 printf ("podaj promień okręgu %lf\n", r);
 scanf ("%lf", &r);
 printf ("%d*%lf*%lf=%lf\n", a, M_PI, r, a*M_PI*r);
 getchar();
 getchar();
 return 0;
}
```
obwód kola z dolaczeniem #include <math.h>, żeby liczylo pi /jako M_PI/ ,czyli podstawi samodzielnie wartosć

```c
#include <stdio.h>
#include <math.h>
int main(){
 double r;
 int a;
 a=2;
 printf ("podaj promień okręgu r %lf\n", r);
 scanf ("%lf", &r);
 printf ("%d*%lf*%lf=%lf\n", a, M_PI, r, a*M_PI*r);
 printf ("%lf*%lf=%lf\n", M_PI, r*r, M_PI*r*r);
 getchar();
 getchar();
 return 0;
}
```
obwód i pole kola

```c
#include <stdio.h>
#include <math.h>
int main(){
 double r;
 int a;
 a=2;
 printf ("podaj promień okręgu r %lf\n", r);
 scanf ("%lf", &r);
 printf ("%d*%lf*%lf=%lf Obwod kola\n", a, M_PI, r, a*M_PI*r);
 printf ("%lf*%lf=%lf Pole kola\n", M_PI, r*r, M_PI*r*r);
 getchar();
 getchar();
 
 return 0;
}
```
Pole i obwod z tekstem

```c
#include <stdio.h>
#include <math.h>
int main(){
 double r;
 int a;
 a=2;
 printf ("podaj promień okręgu r %lf\n", r);
 scanf ("%lf", &r);
  puts("Obwod kola");
 printf ("%d*%lf*%lf=%lf\n", a, M_PI, r, a*M_PI*r);
 getchar();
 getchar();
 puts("Pole kola");
 printf ("%lf*%lf=%lf\n", M_PI, r*r, M_PI*r*r);
 getchar();

 return 0;
}
```
Obwód i pole kola z zastosowaniem puts do opisów <br>i podwójnego getchar do przechodzenia dalej enterem

```c
#include <stdio.h>
#include <math.h>
int main(){
 double r;
 int a;
 a=2;
 printf ("podaj promień okręgu r %lf\n", r);
 scanf ("%lf", &r);
 printf ("Obwod kola %lf\n", a*M_PI*r);
 getchar();
 getchar();
 printf ("Pole kola %lf\n", M_PI*r*r);
 getchar();

 return 0;
}
```
Obwód i pole kola bez widocznych obliczen, tylko wynik

```c
#include <stdio.h>
#include <math.h>
int main(){
 double r;
 int a;
 a=2;
 printf ("podaj promień okręgu r %lf\n", r);
 scanf ("%lf", &r);
 printf ("Obwod kola o promieniu %lf wynosi %lf\n", r, a*M_PI*r);
 getchar();
 getchar();
 printf ("Pole kola o promieniu %lf wynosi %lf\n", r, M_PI*r*r);
 getchar();

 return 0;
}
```
Obwód i pole kola z innym opisem

```c
#include <stdio.h>
int main(){
int fahr, celsius;
int lower, upper, step;
lower=0;
upper=300;
step=20;
fahr=lower;
while (fahr<=upper){
      celsius=5*(fahr-32)/9;
      printf("%d\t %d\n", fahr, celsius);
      fahr=fahr+step;
                     }
 getchar();

 return 0;
}
```
zastosowanie while, zamiana stopni F na C od 0 do 300 co 20 F jako cakowite

```c
#include <stdio.h>
int main(){
double fahr, celsius;
int lower, upper, step;
lower=0;
upper=50;
step=1;
fahr=lower;
while (fahr<=upper){
      celsius=5*(fahr-32)/9;
      printf("%.1lf\t %.1lf\n", fahr, celsius);
      fahr=fahr+step;
                     }
 getchar();

 return 0;
}
```
Zastosowanie while. Zamiana stopni F na C od 0 do 50 ale wynik z dokladnocia do jednej po przecinku, <br>czyli zamieniamy int na double i %d na %lf

```c
#include <stdio.h>
int main(){
double fahr, celsius;
int lower, upper, step;
lower=0;
upper=50;
step=1;
fahr=lower;
while (fahr<=upper){
      celsius=5*(fahr-32)/9;
      printf("%5.1lf\t %7.1lf\n", fahr, celsius);
      fahr=fahr+step;
                     }
 getchar();
 return 0;
}
```
Zastosowanie while, to samo ale ladnie wyswietli przecinki jeden pod drugim

```c
#include <stdio.h>
#define LOWER 0
#define UPPER 300
#define STEP 0
int main(){
int fahr, ;
for(fahr=LOWER; fahr<=UPPER; fahr=fahr+STEP)
printf("%3d %6.1lf\n", fahr,(5.0/9.0)*(fahr-32.0));
 getchar();
 return 0;
}
```
zastosowanie for do poprzedniego przykladu #define LOWER 0  i przy #define STEP 0 daje niekonczaca sie petle i żeby wyjsc to ctrl+c<br> zmiana STEP na np. 20 daje normalna petle 

```c
#include <stdio.h>
int main()
{
int u1, u2, u3;/*na kolejne wyrazy ciągu*/
int n;  /*nr wyrazu*/
int i; /*licznik*/
do
  { printf ("podaj numer wyrazu (co najmniej 3): ");
   scanf ("%d", &n);
  }
  while (n<3);
  u2=u1=1; /*dwa pierwsze wyrazy*/
  i=2;
  while (i++ < n) /*dziala tylko dla n>2 i++ najpierw sdprawdza i z n potem zwieksz o jeden*/
   {u3=u1+u2;
    u1=u2;
    u2=u3;
   }
   /*inna możliwość*/
   /*for (i=3; i<=2; i++, u1=u2, u2=u3) u3=u1+u2; */
   printf ("Wyraz o numerze %d ma wartość %d" , n, u3);
 getchar(); getchar();
 return 0;
}
```
Petla do-while 253-257. Program do obliczania n-tego wyrazu (Un) ciagu Fibonacciego

```c
#include <stdio.h>
#define znak '*' /*znak wypelnienia*/
int main()
{
int lbwier;/*calkowita liczba wierszy*/
int lw;  /*licznik wierszy*/
int lodst; /*liczba odstepow poprzedzajacych gwiazdke*/
int j;

  printf ("ile wierszy? ");
   scanf ("%d", &lbwier);
   
   for (lw=0 ; lw<lbwier ; lw++)
   { lodst = lbwier-lw-1;
     for (j=0 ; j<lodst ; j++) putchar (' '); /* putchar-wstaw (' ')-puste miejsce*/
     for (j=0 ; j<2*lw+1 ; j++) putchar (znak); /* (znak)-wstaw * */
     putchar('\n');
   }
 getchar(); getchar();
 return 0;
}
```
Petla for. Trojkat  - choinka o zadeklarowanej liczbie wierszy 

```c
#include <stdio.h>
int main()
{
int i;
i=0;
 for( i=0; i<24; i++)
 {
    printf ("%d\n", i);
 }
 getchar(); getchar();
 return 0;
}  
```
Petla for. Wyswietl liczby od 0 do 23

```c
#include <stdio.h>
int main()
{
int i;
i=0;
 while( i<24)
 {
      printf ("%d\n", i);
      i++;
 }
 getchar(); getchar();
 return 0;
}
```
Petla while. Wyswietl liczby od 0 do 23

```c
#include <stdio.h>
int main()
{
int i,;
i=0;
do
  { printf ("%d\n", i);
  i++;
  }
  while (i<24);
 getchar(); getchar();
 return 0;
} 
```
Petla wdo-while. Wyswietl liczby od 0 do 23

```c
#include <stdio.h>
int main()
{
double i,n;
i=-3.5;
n=7.5;
do
  { printf ("%.1lf\n", i);
  i=i+0.5;
  }
  while (i<=n);
 getchar(); getchar();
 return 0;
} 
```
Petla do-while. Wypisz liczby od - 3.5 do 7.5 z krokiem co 0.5 za pomoca petli do-while.
