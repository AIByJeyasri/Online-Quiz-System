#include <stdio.h>

#define MAX 5

int stack[MAX];
int top = -1;

/* Push operation */
void push(int value)
{
    if (top < MAX - 1)
    {
        stack[++top] = value;
    }
}

/* Pop operation */
int pop()
{
    if (top >= 0)
    {
        return stack[top--];
    }
    return 0;
}

int main()
{
    int answer;
    int score = 0;
    char name[50];

    printf("\n========================================\n");
    printf("          ONLINE QUIZ SYSTEM\n");
    printf("========================================\n");

    printf("\nEnter your name: ");
    scanf("%s", name);

    printf("\nWelcome, %s! 👋\n", name);
    printf("Answer all 5 questions.\n");

    /* Question 1 */
    printf("\n----------------------------------------\n");
    printf("1. Which data structure follows LIFO?\n");
    printf("1) Queue\n");
    printf("2) Stack\n");
    printf("3) Linked List\n");
    printf("4) Tree\n");
    printf("Enter your answer: ");
    scanf("%d", &answer);

    if (answer == 2)
        push(1);
    else
        push(0);

    /* Question 2 */
    printf("\n----------------------------------------\n");
    printf("2. Which data structure follows FIFO?\n");
    printf("1) Stack\n");
    printf("2) Tree\n");
    printf("3) Queue\n");
    printf("4) Graph\n");
    printf("Enter your answer: ");
    scanf("%d", &answer);

    if (answer == 3)
        push(1);
    else
        push(0);

    /* Question 3 */
    printf("\n----------------------------------------\n");
    printf("3. Which data structure is commonly used in BFS?\n");
    printf("1) Stack\n");
    printf("2) Queue\n");
    printf("3) Tree\n");
    printf("4) Array\n");
    printf("Enter your answer: ");
    scanf("%d", &answer);

    if (answer == 2)
        push(1);
    else
        push(0);

    /* Question 4 */
    printf("\n----------------------------------------\n");
    printf("4. Which data structure is used in DFS?\n");
    printf("1) Queue\n");
    printf("2) Stack\n");
    printf("3) Heap\n");
    printf("4) Array\n");
    printf("Enter your answer: ");
    scanf("%d", &answer);

    if (answer == 2)
        push(1);
    else
        push(0);

    /* Question 5 */
    printf("\n----------------------------------------\n");
    printf("5. Which data structure consists of nodes connected by links?\n");
    printf("1) Linked List\n");
    printf("2) Stack\n");
    printf("3) Queue\n");
    printf("4) Array\n");
    printf("Enter your answer: ");
    scanf("%d", &answer);

    if (answer == 1)
        push(1);
    else
        push(0);

    /* Calculate score using stack */
    while (top != -1)
    {
        score = score + pop();
    }

    /* Result */
    printf("\n========================================\n");
    printf("              QUIZ RESULT\n");
    printf("========================================\n");

    printf("Name  : %s\n", name);
    printf("Score : %d / 5\n", score);

    if (score >= 3)
    {
        printf("\n        *** CONGRATULATIONS! ***\n");
        printf("             RESULT: PASS\n");
        printf("        Excellent Performance!\n");
    }
    else
    {
        printf("\n          Keep Practicing!\n");
        printf("             RESULT: FAIL\n");
        printf("       Better luck next time!\n");
    }

    printf("\n========================================\n");
    printf("           Thank You!\n");
    printf("========================================\n");

    return 0;
}
