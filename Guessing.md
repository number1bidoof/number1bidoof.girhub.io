```mermaid
flowchart TD
    1([Start the game]) --> 2[/What is your name?/]
    2-->3[Hello Name, welcome to the game pick a number between 1-100]
    3-->4{User picks a number between 1-100}
    4 -->|user guesses correctly| 5(Congrats, you guessed correctly, would you like to play again)
    5 --> |user picks to play again| 1
    5 --> |user picks to not play again| 10([End of the game])
    4 --> |user picks a number that is too big| 6(Sorry, your number is way too big, please pick another number that is smaller)
    8(user is prompted to pick another number) 
    6 --> 8
    8 --> |user picks another number|4
    4 --> |user picks a number that is too small| 7(Sorry, you number is too small, pick another number that is larger)
    7 --> 8
    4 --> |the number inputed is NOT a numerical value| 9(This value is not a number, please pick a value that is in the proper range) 
    9 --> 8  
```

In this diagram, the user is first promted to give their name. Then they are prompted to give a number. If they win, they are able to play the game again or quit, where the loop end. Based on the users answer the game will tell them if thier answer is too big or too small or too big, and sugest to them to answer further to the answer. the user gets unlimted atempts and the range of answers is between 1-100