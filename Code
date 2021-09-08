mark = ("X", "O")
player = 0
step = 1
GameWin = False
GameArea = [["-", "-", "-"],["-", "-", "-"],["-", "-", "-"]]

def Draw (Arr):
    print ("   1  2  3")
    for row in range(3):
        print(f'{row+1}  '+'  '.join(Arr[row]))
    print ()

def IfWin(Arr, r):
    a = 0
    for a in range(3):
        # Проверка по столбцам
        if Arr[0][a] == mark[r] and Arr[1][a] == mark[r] and Arr[2][a] == mark[r]: 
            return  True
        # Проверка по строкам
        if Arr[a][0] == mark[r] and Arr[a][1] == mark[r] and Arr[a][2] == mark[r]:
            return  True 
    # Проверка по диагонали left/right
    if Arr[0][0] == mark[r] and Arr[1][1] == mark[r] and Arr[2][2] == mark[r]:
       return  True  
    # Проверка по диагонали right/left
    if Arr[2][0] == mark[r] and Arr[1][1] == mark[r] and Arr[0][2] == mark[r]:
        return  True
    return False

Draw (GameArea)

while GameWin == False:
    player = step % 2
    print("Ход -> " + mark[player])
    x, y = map(int, input().split())
    
    if GameArea[y-1][x-1] == "-":
        GameArea[y-1][x-1] = mark[player]
    else: 
        print ("Эта клетка уже занята")
    Draw (GameArea)
    GameWin = IfWin(GameArea, player)
    if GameWin == True:
        print ("Победили " + str(mark[player]))
    step += 1
