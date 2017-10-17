# Tempo-em-dia

#include <stdio.h>


int main(void)
{
    int w,x=0,y,z;
    int k,l;
    int h,m,s;
    int hh, mm, ss;

    printf("Dia ");
    scanf("%d",&k);
    scanf("%d : %d : %d",&h,&m,&s);
    printf("Dia ");
    scanf("%d",&l);
    scanf("%d : %d : %d",&hh,&mm,&ss);

    w = l - k; /*w recebe o primeiro dia menos o segundo dia*/

    if(h > hh)  /*Verifica se a primeira hora é maior que a segunda*/
    {
        w = w-1;
    }

    x = x + (h + hh);
    x = x + h;    /*x recebe as horas*/

    while(x>24) /*Enquanto as horas não forem menores que 24*/
    {
    if(x > 24)
    {
        x = x-24;
        w++;
    }
    }

    if(m > mm)
    {
        y = m - mm;    /*y recebe o primeiro minuto menos o segundo minuto*/
    }
    else if(m < mm)
    {
        y = mm - m;
    }

        /*Verificação de segundos*/

    if(s == ss)
    {
        z = 0;
    }
    else if(s > ss)
    {
        z = s - ss;
    }
    else if(ss > s)
    {
        z = ss - s;
    }

        /*IMpressão do problema*/

        printf("%d dia(s)\n",w);
        printf("%d hora(s)\n",x);
        printf("%d minuto(s)\n",y);
        printf("%d segundo(s)\n",z);

    return 0;
}
