# jaswant
import random
Cchoice=['Rock','Paper','Scissor']
while True:
    print('Rock Paper Scissor Game:')
    youwin,computerwin=0,0
    for i in range(1,6):
        print('Round',i,'start:')
        print('Please select any one option:')
        print('1.Rock','2.Paper','3.Scissor',sep='\n')
        Yourchoice=int(input())
        if Yourchoice==1:
            print('You select Rock')
            Yourchoice='Rock'
        elif Yourchoice==2:
            print('You select Paper')
            Yourchoice='Paper'
        elif Yourchoice==3:
            print('You select Scissor')
            Yourchoice='Scissor'
        else:
            print('Invalid choice')
            break
        Computerchoice=random.choice(Cchoice)
        print('Computer select :',Computerchoice)

        if Yourchoice==Computerchoice:
            youwin+=1
            computerwin+=1
            print('This round is drawn:')
        elif (Yourchoice=='Paper' and Computerchoice=='Rock')or (Yourchoice=='Rock' and Computerchoice=='Scissor') or (Yourchoice=='Scissor' and Computerchoice=='Paper'):
            youwin+=1
            print('You win this round')
        else:
            computerwin+=1
            print('Computer win this round')
    if youwin>computerwin:
        print('You win the game:')
        print('Score is:','Your score:',youwin,'computer score:',computerwin,sep=' ')
    elif computerwin>youwin:
        print('You lose the game .Computer win the game')
        print('Score is:','Your score:',youwin,'computer score:',computerwin,sep=' ')
    else:
        print('Match Drawn')
        print('Score is:','Your score:',youwin,'computer score:',computerwin,sep=' ')
    User_choice=input('Want to play again? (yes/Exit)')
    if User_choice=='Yes' or User_choice=='yes' or User_choice=='YES':
        continue
    else:
        break
