# Swit in c

faça um algoritmo que simule o funcionamento de um caixa eletrônico, onde será apresentado uma lista de operações:

1-Saldo

2-Saque

3-Deposito

Ao iniciar o programa determine um valor inicio para a variável saldo, se o cliente escolher a opção 1 mostre o valor do saldo, 

caso escolha o valor 2 leia o valor a ser sacado e verifique se existe saldo suficiente, se o saldo for maior ou igual , deduza 

da variável saldo o valor solicitado, caso não haja saldo suficiente mostre a mensagem “Saldo Insuficiente”, 

caso a opção 3 seja escolhida adicione o valor informado de deposito ao saldo.

```c
#include <stdio.h>

int main()
{
  
    int op; 
    float saque, deposito; 
    float saldo = 1500;
    
    printf("Informe uma opção de escolha para vereficação: 1-Saldo, 2-Saque, 3-Deposito\n");
    scanf("%i", &op);
   
   
    switch(op){
        case 1: {
            printf("O seu saldo é de R$ %.2f\n", saldo);
            break;
        }
        case 2: {
            printf("Insira o valor do saque:\n");
            scanf("%f", &saque);
            if(saldo>= saque){
                saldo = saldo - saque;
                printf("O saque foi descontado do valor do saldo e o saldo atual será de:R$ %.2f\n", saldo);
            } else {
               if(saldo<saque){
                   printf("Saldo insuficiente!!\n");
               }
            }
            break;
        }
        case 3:{
           printf("Insira o valor do deposito:\n");
           scanf("%f", &deposito);
                saldo = saldo + deposito;
                printf("Foi depositado o valor de: R$ %.2f e o saldo atual é de R$ %.2f\n", deposito, saldo);
                break;
        }
        default :{
            printf("\n operacao invalida !!!\n");
        }
    }
    return 0;
}

```

