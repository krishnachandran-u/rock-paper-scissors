#include <stdio.h>
#include <stdlib.h>
#include <conio.h>

const char* rock_paper_scissors(char p1, char p2){

    if((p1 != 'r' && p1 != 's' && p1 != 'p') || (p2 != 'r' && p2 != 's' && p2 != 'p')) return "Invalid entry"; //If either p1 or p2 holds an inadmissible character

    if(p1 == p2) return "TIE"; //If p1 and p2 are the same

    if((p1 == 'r' && p2 == 's') || (p1 == 's' && p2 == 'p') || (p1 == 'p' && p2 == 'r')) return "Player 1 wins"; else return "Player 2 wins"; //Case for winning

}

int main(){

    char p1, p2;

    printf("r -> ROCK; p -> PAPER; s -> SCISSOR\n\n");

        printf("P1: "); p1 = getch();
        printf("\nP2: "); p2 = getch();

        printf("\n");

    printf("\nP1: %c; P2: %c",p1,p2);
    printf("\n%s",rock_paper_scissors(p1, p2));

    return 1;
}
