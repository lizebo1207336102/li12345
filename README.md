# li12345
数当てゲーム
//in this case,i will write a game by C language

//you will see the code


    #include <stdio.h>
    #include <stdlib.h>
    #include <time.h>

    int main() {
        int answer, guess, num_guesses = 0;
        srand(time(NULL)); // 乱数のシードを初期化する
        answer = rand() % 100 + 1; // 1から100までのランダムな数を生成する

        printf("1から100までの数を当ててください。\n");

        while (1) {
            printf("予想した数を入力してください: ");
            scanf("%d", &guess);
            num_guesses++;
            if (guess == answer) {
                printf("正解です！%d回目で当たりました。\n", num_guesses);
                break;
            } else if (guess < answer) {
                printf("もっと大きな数です。\n");
            } else {
                printf("もっと小さな数です。\n");
            }
        }

        return 0;
    }
