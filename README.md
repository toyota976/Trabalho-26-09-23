# Trabalho-26-09-23
Acertar o numero de 1 a 10 com multiplos jogadores
#include <stdio.h>
#include <stdlib.h>
#include <time.h>

int main()
{
    int jogador=0, num_j=1, chute=0;
    srand(time(0));
    int aleatorio = rand() % 10 + 1;
    printf("%d",aleatorio);
    
    printf("\nDigite a quantidade de jogadores: ");
    scanf("%d",&num_j);
    printf("\nO jogo so para quando um jogador acertar");
    
        for(int i=1; i<=num_j; i++){
        printf("\nJogador %d :",i);
        scanf("%d",&jogador);
        if(jogador == aleatorio){
            printf("Jogador %d ganhou!!",i);
            break;
        }
        chute++;
        if(i == num_j){
            i=0;
        }
    }
    printf("Fim de jogo!! O total de chutes foi de %d",chute);
}
