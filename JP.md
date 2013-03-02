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
