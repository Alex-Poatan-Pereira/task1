# laughing-octo-adventure
import random as rd
rd = int(rd.randrange(1,11)) #randrange로 랜덤한 숫자의 범위 형성(1~10)
# print(rd)            
# random을 이용해서 랜덤 값 주기, print를 사용해 제대로 작동하는지 시행

print(f"1에서 10 사이의 숫자를 정했습니다. 맞춰보시죠 닝겐")

# input(f"숫자를 입력하세요")
# #사용자가 숫자를 입력하도록 input을 입력, input을 통해 입력된 값은 '문자열' 이기 떄문에 정수형으로 변환해야 함


# int(input(f"숫자를 입력하세요"))
#int()로 정수형으로 값이 나오도록 설정

#input_number = int(input(f"숫자를 입력하세요"))

# if input_number > rd :
#     print(f"Down")
# elif input_number < rd :
#     print(f"Up")
# else :
#     print(f"정답입니다!")
# #이 경우 숫자를 1번만 입력하면 게임이 끝나게 된다..


while True:
    input_number = int(input(f"숫자를 입력하세요"))
    if input_number == rd:   # =이 안된다. 값이 같다는건 '=='만 써야하나보다
        print(f"정답입니다!") 
        input_yn = input(f"좀 하는군. 한 판 더?(콜/노잼)")
        if input_yn == "콜":      #콜을 입력한 경우 다시 시작한다는 문구를 보여줌
            print(f"게임을 다시 시작합니다")
            import random as rd    #번호도 다시 랜덤하게 선택됨
            rd = int(rd.randrange(1,11))
            continue              #아래내용 건너뛰기
        else:    
            print(f"바보")
        break                     
    if input_number < rd:     
        print(f"Up")
        continue         #작은 숫자를 입력했을 때 up을 보여주고 아래에 있는 프린트문은 건너뜀
    print(f"Down")       #위에 모두 해당 안될때 down을 보여줌
