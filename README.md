 //Jogo de Quiz em C
// Atividade Pontuada EXTRA

#include <stdio.h>
#include <stdlib.h>
#include <ctype.h>

// Prototipação das funções
void exibirRegras();
int iniciarQuiz();
void exibirResultado(int pontos);

int main() {
    exibirRegras();
    int pontos = iniciarQuiz();
    exibirResultado(pontos);
    return 0;
}

void exibirRegras() {
    printf("\n>>> VER REGRAS <<<\n");
    printf("----------------------------------------\n");
    printf("COMO JOGAR:\n");
    printf("1. O quiz possui 5 perguntas sobre Filmes e Series\n");
    printf("2. Cada pergunta tem 3 alternativas (a, b, c)\n");
    printf("3. Cada resposta correta vale 2 pontos\n");
    printf("4. Pontuacao maxima: 10 pontos\n");
    printf("5. Responda com a letra da alternativa\n");
    printf("----------------------------------------\n");
    printf("Boa sorte e divirta-se!\n\n");
}

int iniciarQuiz() {
    char resposta;
    int pontos = 0;

    printf("\n========== QUIZ FILMES E SERIES ==========\n\n");

    printf("Pergunta 1: Quem é o vilão de 'Vingadores Guerra Infinita'?\n");
    printf("a) Loki\nb) Thanos\nc) Ultron\nSua resposta: ");
    scanf(" %c", &resposta);
    if (tolower(resposta) == 'b') {
        printf("Correto!\n\n");
        pontos += 2;
    } else {
        printf("Incorreto! A resposta correta é 'b'\n\n");
    }

    printf("Pergunta 2: Em que casa de Hogwarts Harry Potter foi selecionado?\n");
    printf("a) Sonserina\nb) Corvinal\nc) Grifinória\nSua resposta: ");
    scanf(" %c", &resposta);
    if (tolower(resposta) == 'c') {
        printf("Correto!\n\n");
        pontos += 2;
    } else {
        printf("Incorreto! A resposta correta é 'c'\n\n");
    }

    printf("Pergunta 3: Qual é o nome do planeta natal do Superman?\n");
    printf("a) Terra\nb) Krypton\nc) Saturno\nSua resposta: ");
    scanf(" %c", &resposta);
    if (tolower(resposta) == 'b') {
        printf("Correto!\n\n");
        pontos += 2;
    } else {
        printf("Incorreto! A resposta correta é 'b'\n\n");
    }

    printf("Pergunta 4: Em 'Stranger Things', qual o nome do mundo paralelo?\n");
    printf("a) Mundo Invertido\nb) Submundo\nc) Outra Dimensao\nSua resposta: ");
    scanf(" %c", &resposta);
    if (tolower(resposta) == 'a') {
        printf("Correto!\n\n");
        pontos += 2;
    } else {
        printf("Incorreto! A resposta correta é 'a'\n\n");
    }

    printf("Pergunta 5: Quem dirigiu o filme 'Titanic' (1997)?\n");
    printf("a) Steven Spielberg\nb) James Cameron\nc) Christopher Nolan\nSua resposta: ");
    scanf(" %c", &resposta);
    if (tolower(resposta) == 'b') {
        printf("Correto!\n\n");
        pontos += 2;
    } else {
        printf("Incorreto! A resposta correta é 'b'\n\n");
    }

    return pontos;
}

void exibirResultado(int pontos) {
    printf("\n========== RESULTADO FINAL ==========\n");
    printf("Pontuação total: %d pontos\n", pontos);

    if (pontos <= 4) {
        printf("Precisa estudar mais!\n");
    } else if (pontos <= 8) {
        printf("Muito bem!\n");
    } else if (pontos == 10) {
        printf("Excelente, parabéns!\n");
    }

    printf("=====================================\n\n");
}
