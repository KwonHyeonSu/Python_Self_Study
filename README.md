# Python_Self_Study
Python_Self_Study

### 링크 : https://www.youtube.com/watch?v=kWiCuklohdY&t=315s

int(3.5) -> 3 #정부부분만 출력   

print("z"*9) -> ㅋㅋㅋㅋㅋㅋㅋㅋㅋ   
정수형을 프린트 : str(age)   

print(2**3) -> 8   

print(7/3) -> 2.3333   
print(7//3) -> 2   
print(7%3) -> 1   

not, and(&), or(|)   

abs(-5) -> 5   
pow(4,2) -> 16   
max(5,12) -> 12   
min(5,12) -> 5   
round(3.14) -> 3 (반올림)   

from math import * -> math 라이브러리 내의 모든 기능을 이용
   
> floor(4.99) -> 4 #내림      
> ceil(3.14) -> 4 #올림      
> sqrt(16) -> 4 #제곱근     

from random import *

random() -> 0.0 ~ 1.0 임의의 값   
randrange(1,46) #1~45   
randint(1,45) #1~45

# 문자열 포맷

#방법1
print("나는 %d살입니다." % 20)
print("나는 %s를 좋아해요." % "파이썬")
print("Apple은 %c로 시작해요" % "A")

print("나는 %s살입니다." % 20)
print("나는 %s색과 %s색을 좋아해요."% ("파란", "빨간"))


#방법2
print("나는 {}살입니다.".format(20))
print("나는 {0}색과 {1}색을 좋아해요.".format("파란", "빨간"))

#방법3
print("나는 {age}살이며, {color}색을 좋아해요.".format(age = 20, color = "빨간"))

#방법4
age = 20
color = "빨간"
print(f"나는 {age}살이며, {color}색을 좋아해요.")


# 사전

cabinet = {3:"유재석", 100:"김태호"}   
print(cabinet[3]) #유재석   
print(cabinet[100]) #김태호   

print(cabinet.get(3)) #유재석   
#print(cabinet[5]) #오류나고 프로그램 종료   
print(cabinet.get(5)) #오류 안나고 None 반환   
print("hi")   

print(3 in cabinet) #True   
print(5 in cabinet) #False   

cabinet = {"A-3":"유재석", "B-100":"김태호"}   
print(cabinet["A-3"])   
print(cabinet["B-100"])   

#새 손님   
print(cabinet)   
cabinet["A-3"] = "김종국"   
cabinet["C-20"] = "조세호"   
print(cabinet)   

#간 손님   
del cabinet["A-3"]   
print(cabinet)   

#ket 들만 출력    
print(cabinet.keys())   

#value 만 출력   
print(cabinet.values())   

#key, value 쌍으로 출력   
print(cabinet.items())   

cabinet.clear()   
print(cabinet)   

#튜플
#리스트는 []로 둘러싸지만, 튜플은 ()으로 둘러싼다.   
#리스트는 그 값의 생성, 삭제 수정이 가능하지만 튜플은 그 값을 바꿀 수 없다.   

menu = ("돈까스", "치즈까스")   
print(menu[0])  
print(menu[1])  

#menu.add("생선까스")  

#name = "김종국"  
#age = 20  
#hobby = "코딩"  
#print(name, age, hobby)  

(name, age, hobby) = ("김종국", 20, "코딩")  
print(name, age, hobby)  


# 세트(set : 집합)
#중복 안됨, 순서 없음   
my_set = {1,2,3,3,3}   
print(my_set)   

java = {"유재석", "김태호", "양세형"}  
python = set(["유재석", "박명수"])  

#교집합 (java 와 python을 모두 할 수 있는 개발자)  
print(java & python)  
print(java.intersection(python))  

#합집합 (java를 할 수 있거나 python 할 수 있는 개발자)  
print(java | python)  
print(java.union(python))  

#차집합 (java 할 수 있지만 python은 할 줄 모르는 개발자)  
print(java - python)  
print(java.difference(python))  

#파이선 할 줄 아는사람 늘어남  
python.add("김태호")  
print(python)  

#java를 잊었어요  
java.remove("김태호")  
print(java)  


# 퀴즈
from random import *

users = range(1, 21)
users = list(users)

print(users)
shuffle(users)
print(users)

winners = sample(users, 4)

print("-- 당첨자 발표 --")
print("치킨 당첨자 : {0}".format(winners[0]))
print("커피 당첨자 : {0}".format(winners[1:]))
print("-- 축하합니다 --")

# if

weather = input("오늘 날씨는 어때요? ")
if weather == "비" or weather == "눈":
    print("우산을 챙기세요")
elif weather == "미세먼지":
    print("마스크를 챙기세요")
else:
    print("준비물 필요 없어요.")

temp = int(input("기온은 어때요? "))
if 30 <= temp:
    print("너무 더워요. 나가지 마세요")
elif 10 <= temp and temp < 30 :
    print("괜찮은 날씨에요")
elif 0<= temp and temp <10:
    print("외투를 챙기세요")
else:
    print("너무 추워요. 나가지 마세요")

# for
for waiting_no in range(1, 6): #1,2,3,4,5
    print("대기번호 : {0}".format(waiting_no))

starbucks = ["아이언맨", "토르", "아이엠 그루트"]
for customer in starbucks:
    print("{0}, 커피가 준비되었습니다.".format(customer))
    
# while

customer = "토르"
index = 5
while index >= 1:
    print("{0} 커피가 준비 되었습니다. {1}번 남았어요.".format(customer, index))
    index -= 1
    if index==0 :
        print("커피는 폐기처분되었습니다.")

'''
customer = "아이언맨"
index = 1
while True:
    print("{0} 커피가 준비 되었습니다. 호출 {1}회".format(customer, index))
    index += 1
'''

customer = "토르"
person = "Unknown"

while person != customer:
    print("{0} 커피가 준비되었습니다.".format(customer))
    person = input("이름이 어떻게 되세요? ")

# continue, break  

absent = [2,5] #결석  
no_book = [7] #책을 깜빡했음  
for student in range(1, 11): #1,2,3,4,5,6,7,8,9,10  
    if student in absent:  
        continue #코드 실행 건너 뜀  
    elif student in no_book:  
        print("오늘 수업 여기까지. {0}는 교무실로 따라와".format(student))  
        break  
    print("{0}, 책을 읽어봐".format(student))  

# for한줄

#출석번호가 1 2 3 4 ,앞에 100을 붙이기로 함 -> 101, 102, 103, 104.   
student = [1,2,3,4,5]   
print(student)  
student = [i+100 for i in student]  
print(student)  
  
#학생 이름을 길이로 변환  
student = ["Iron man", "Thor", "I am groot"]  
student = [len(i) for i in student]  
print(student)  

#학생 이름을 대문자로 변환
student = ["Iron man", "Thor", "I am groot"]  
student = [i.upper() for i in student]  
print(student)  


# 퀴즈

from random import *  
  
cnt = 0 #총 탑승 승객 수  
for i in range(1, 51): #1~50  
    time = randrange(5, 51) #5분 ~ 50분  
    if 5<= time <= 15:  
        print("[0] {0}번째 손님 (소요시간 : {1}분)".format(i, time))  
        cnt += 1
    else:
        print("[ ] {0}번째 손님 (소요시간 : {1}분)".format(i, time))

print("총 탑승 승객 : {0} 분".format(cnt))


# 함수    
  
def open_account():    
    print("새로운 계좌가 생성되었습니다.")    

def deposit(balance, money): #입금  
    print("입금이 완료되었습니다. 잔액은 {0} 원입니다.".format(balance + money))  
    return balance + money  
  
def withdraw(balance, money):  
    if balance > money:  
        print("출금이 완료되었습니다. 잔액은 {0} 원입니다.".format(balance-money))  
        return balance-money  
    else:  
        print("출금이 완료되지 않았습니다. 잔액은 {0} 원입니다.".format(balance))  
        return balance  
  
def withdraw_night(balance, money): #저녁에 출금  
    commission = 100 #수수료 100원  
    return commission, balance - money - commission  
  
balance = 0 #잔액  
balance = deposit(balance, 1000)  
balance = withdraw(balance, 2000)  
commision, balance = withdraw_night(balance, 500)  
print("수수료 {0}원이며, 잔액은 {1}원입니다.".format(commision, balance))    

## 기본값

def profile(name, age, main_lang):  
    print("이름 : {0}\t나이 : {1}\t주 사용 언어 : {2}"\  
        .format(name, age, main_lang))  

profile("유재석", 20, "파이선")  
profile("김태호", 25, "자바")  

#같은 학교 같은 학년 같은 반 수업.  

def profile(name, age = 17, main_lang = "파이썬"):  
    print("이름 : {0}\t나이 : {1}\t주 사용 언어: {2}"\  
        .format(name, age, main_lang))  

profile("유재석")  
profile("김태호")  


## 키워드값

def profile(name, age, main_lang):  
    print(name, age, main_lang)  

profile(name = "유재석", main_lang =  "파이썬", age = 20)  
profile(main_lang = "자바", age = 25, name = "김태호")  


## 가변인자

'''  
def profile(name, age, lang1, lang2, lang3, lang4, lang5):  
    print("이름 : {0}\t나이 : {1}\t".format(name, age), end = "")  
    print(lang1, lang2, lang3, lang4, lang5)  
'''  
def profile(name, age, *language):  
    print("이름 : {0}\t나이 : {1}\t".format(name, age), end = "")  
    for lang in language:  
        print(lang, end = " ")  
    print()  
  
profile("유재석", 20, "Python", "Java", "C", "C++", "C#")  
profile("김태호", 25, "Kotlin", "Swift")  

# 지역변수와 전역변수   
gun = 10  

def checkpoint(soldiers): #경계근무  
    global gun  
    gun = gun - soldiers  
    print("[함수 내] 남은 총 : {0}".format(gun))  
  
def checkpoint_ret(gun, soldiers):  
    gun = gun - soldiers  
    print("[함수 내] 남은 총 : {0}".format(gun))  
    return gun  
  
print("전체 총 : {0}".format(gun))  
checkpoint(2)  
gun = checkpoint_ret(gun, 2)  
print("전체 총 : {0}".format(gun))  

# 표준 입출력  
scores = {"수학":0, "영어":50, "코딩":100}  
for subject, score in scores.items():   
    print(subject.ljust(8), str(score).rjust(4), sep=":")  

#은행 대기순번표  
#001, 002, 003, ...  
for num in range(1, 21):  
    print("대기번호 : " + str(num).zfill(3))  
  
answer = input("아무 값이나 입력하세요 : ")  
answer = 10  
print(type(answer))  
print("입력하신 값은 " + answer + "입니다.")  


# 출력 포맷   

#빈 자리는 빈공간으로 두고, 오른쪽 정렬을 하되, 총 10자리 공간을 확보  
print("{0: >10}".format(500))  
#양수일 땐 +로 표시, 음수일 땐 -로 표시  
print("{0: >+10}".format(500))  
print("{0: >10}".format(-500))  
  
#왼쪽 정렬하고, 빈칸으로 _로 채움  
print("{0:_<+10}".format(500))  
  
#3자리 마다 콤마를 찍어주기  
print("{0:,}".format(100000000000))  
  
#3자리 마다 콤마를 찍어주기, +-부호도 붙이기  
print("{0:+,}".format(100000000000))  
print("{0:+,}".format(-100000000000))  
  
#3자리 마다 콤마를 찍어주기, 부호도 붙이고, 자릿수 확보하기  
#돈이 많으면 행복하니까 빈 자리는 ^로 채워주기  
print("{0:^<+30,}".format(100000000000))  
  
#정리 - 각 자리별로 들어가야 하는 것 : print("{0:빈칸채우기 정렬여부 부호 차지하는자릿수 3자리마다콤마".format(~~~))  
  
#소수점 출력  
print("{0:f}".format(5/3))  
  
#소수점 특정 자리수 까지만 표시  
print("{0:.2f}".format(5/3))     

# 파일 입출력  
  
'''  
#파일 쓰기  
score_file = open("score.txt", "w", encoding = "utf8")  
print("수학 : 0", file=score_file)  
print("영어 : 50", file=score_file)  
score_file.close()  
  
score_file = open("score.txt", "a", encoding="utf8")  
score_file.write("과학 : 80\n")  
score_file.write("코딩 : 100")  
score_file.close()  
  
'''  
  
'''  
#한줄씩 받기  
score_file = open("score.txt", "r", encoding = "utf8")  
print(score_file.readline(), end="") #줄별로 읽기, 한 줄 읽고 커서는 다음 줄로 이동  
print(score_file.readline(), end="")  
print(score_file.readline(), end="")  
print(score_file.readline(), end="")  
score_file.close()  
  
'''  
  
'''  
#파일이 총 몇 줄인지 모를 때  
score_file = open("score.txt", "r", encoding="utf8")  
while True:  
    line = score_file.readline()  
    if not line:   
        break  
    print(line, end="")  
score_file.close()  
  
'''  
  
score_file = open("score.txt", "r", encoding="utf8")  
lines = score_file.readlines() #list 형태로 저장  
for line in lines:  
    print(line, end="")  
score_file.close()    


# pickle  
  
'''  
#피클 쓰기  
  
import pickle  
profile_file = open("profile.pickle", "wb")  
profile = {"이름":"박명수", "나이":30, "취미":["축구","골프","코딩"]}  
print(profile)  
pickle.dump(profile, profile_file) #profile에 있는 정보를 file에 저장  
profile_file.close()  
  
'''  
  
#피클 읽기  
  
import pickle  
profile_file = open("profile.pickle", "rb")  
profile = pickle.load(profile_file) #file에 있는 정보를 profile에 불러오기  
print(profile)  
profile_file.close()  


# with - 파일처리 쉽게함 - close 적을 필요 없음  
'''  
  
with open("study.txt", "w", encoding="utf8") as study_file:  
    study_file.write("파이썬을 열심히 공부하고 있어요")  
  
'''  
  
with open("study.txt", "r", encoding="utf8") as study_file:  
    print(study_file.read())  


# 클래스  
  
class Unit:  
    def __init__(self, name, hp, damage):  
        self.name = name  
        self.hp = hp  
        self.damage = damage  
        print("{0} 유닛이 생성 되었습니다.".format(self.name))  
        print("체력 {0}, 공격력 {1}".format(self.hp, self.damage))  
  
  
marine1 = Unit("마린", 40, 5)  
marine2 = Unit("마린", 40, 5)  
tank = Unit("탱크", 150, 35)  

# 클래스  
  
class Unit:   
    def __init__(self, name, hp, damage):  
        self.name = name  
        self.hp = hp  
        self.damage = damage  
        print("{0} 유닛이 생성 되었습니다.".format(self.name))  
        print("체력 {0}, 공격력 {1}".format(self.hp, self.damage))  
  
  
marine1 = Unit("마린", 40, 5)   
marine2 = Unit("마린", 40, 5)    
tank = Unit("탱크", 150, 35)    
 
#레이스 : 공중 유닛, 비행기. 클로킹 (상대방에게 보이지 않음)  
wraith1 = Unit("레이스", 80, 5)  
print("유닛 이름 : {0}, 공격력 : {1}".format(wraith1.name, wraith1.damage))  
  
#마인드 컨트롤 스킬  
wraith2 = Unit("빼앗은 레이스", 80, 5)  
wraith2.clocking = True  
  
if wraith2.clocking == True:  
    print("{0} 는 현재 클로킹 상태입니다.".format(wraith2.name))  
  
# 클래스  


#일반 유닛  
class Unit:   
    def __init__(self, name, hp):  
        self.name = name  
        self.hp = hp   

class AttackUnit(Unit):
    def __init__(self, name, hp, damage):  
        Unit.__init__(self, name, hp)  
        self.damage = damage  

    def attack(self, location):  
        print("{0} : {1} 방향으로 적군을 공격 합니다. [공격력 {2}]"\
            .format(self.name, location, self.damage))  
  
    def damaged(self, damage):  
        print("{0} : {1} 데미지를 입었습니다.".format(self.name, damage))  
        self.hp -= damage  
        print("{0} : 현재 체력은 {1} 입니다.".format(self.name, self.hp))  
        if(self.hp <= 0):  
            print("{0} : 파괴되었습니다.".format(self.name))  
  
  
#파이어뱃 : 공격 유닛, 화염방사기.  
firebat1 = AttackUnit("파이어뱃", 50, 16)  
firebat1.attack("5시")  
  
firebat1.damaged(25)  
firebat1.damaged(25)  

# 클래스  


#일반 유닛  
class Unit:   
    def __init__(self, name, hp):  
        self.name = name  
        self.hp = hp   

class AttackUnit(Unit):
    def __init__(self, name, hp, damage):  
        Unit.__init__(self, name, hp)  
        self.damage = damage  

    def attack(self, location):  
        print("{0} : {1} 방향으로 적군을 공격 합니다. [공격력 {2}]"\  
            .format(self.name, location, self.damage))  
  
    def damaged(self, damage):  
        print("{0} : {1} 데미지를 입었습니다.".format(self.name, damage))   
        self.hp -= damage  
        print("{0} : 현재 체력은 {1} 입니다.".format(self.name, self.hp))    
        if(self.hp <= 0):    
            print("{0} : 파괴되었습니다.".format(self.name))    

#드랍쉽 : 공중 유닛, 수송기. 마린 / 파이어뱃 / 탱크 등을 수송. 공격 X  

#날 수 있는 기능을 가진 클래스  
class Flyable:  
    def __init__(self, flying_speed):  
        self.flying_speed = flying_speed  

    def fly(self, name, location):  
        print("{0} : {1} 방향으로 날아갑니다. [속도 {2}]"\  
            .format(name, location, self.flying_speed))  

#공중 공격 유닛 클래스  
class FlyableAttackUnit(AttackUnit, Flyable):  
    def __init__(self, name, hp, damage, flying_speed):  
        AttackUnit.__init__(self, name, hp, damage)  
        Flyable.__init__(self, flying_speed)  

#발키리 : 공중 공격 유닛, 한번에 14발 미사일 발사.  
valkyrie = FlyableAttackUnit("발키리", 200, 6, 5)  
valkyrie.fly(valkyrie.name, "3시")  

# super
#건물
class BuildingUnit(Unit):
    def __init__(self, name, hp, location):
        #Unit.__init__(self, name, hp, 0)
        super().__init__(name, hp, 0)
        self.location = location
        
# 퀴즈
class House:  
    def __init__(self, location, house_type, deal_type, price, completion_year):    
        self.location = location  
        self.house_type = house_type  
        self.price = price  
        self.deal_type = deal_type  
        self.completion_year = completion_year  
      
    def show_detail(self): 
        print(self.location , self.house_type, self.deal_type\  
            ,self.price, self.completion_year)  
      
houses = []  
house1 = House("강남", "아파트", "매매", "10억", "2010년")  
house2 = House("마포", "오피스텔", "전세", "5억", "2007년")    
house3 = House("송파", "빌라", "월세", "500/50", "2000년") 
houses.append(house1)   
houses.append(house2) 
houses.append(house3)   
  
print("총 {0}대의 매물이 있습니다.".format(len(houses)))  
for house in houses:  
    house.show_detail()  
  
# 예외처리

try:  
  
    print("나누기 전용 계산기입니다.")  
    nums = []  
    nums.append(int(input("첫 번째 : ")))  
    nums.append(int(input("두 번째 : ")))
    #nums.append(int(nums[0] / nums[1]))
  
    print("{0} / {1} = {2}".format(nums[0], nums[1], nums[2]))  
  
except ValueError:  
    print("에러! 잘못된 값을 입력하였습니다.")  
  
except ZeroDivisionError as err:  
    print(err)  

except Exception as err: #나머지 모든 오류  
    print("알 수 없는 에러가 발생하였습니다.") 
    print(err)   
    
# 일부러 에러 발생
  
try:  
    print("한 자리 숫자 나누기 전용 계산기입니다.")  
    num1 = int(input("첫 번째 숫자를 입력하세요 : "))  
    num2 = int(input("두 번째 숫자를 입력하세요 : "))  
    if num1 >= 10 or num2 >= 10:  
        raise ValueError  
    print("{0} / {1} = {2}".format(num1, num2, int(num1 / num2)))  
  
except ValueError:  
    print("잘못된 값을 입력하였습니다. 한 자리 숫자만 입력하세요")  
  

# 사용자 정의 예외처리  

class BigNumberError(Exception):  
    def __init__(self, msg):  
        self.msg = msg  

    def __str__(self):  
        return self.msg  
  
try:    
    print("한 자리 숫자 나누기 전용 계산기입니다.")    
    num1 = int(input("첫 번째 숫자를 입력하세요 : "))    
    num2 = int(input("두 번째 숫자를 입력하세요 : "))    
    if num1 >= 10 or num2 >= 10:    
        raise BigNumberError("입력값 : {0}, {1}".format(num1, num2))    
    print("{0} / {1} = {2}".format(num1, num2, int(num1 / num2)))    
    
except ValueError:    
    print("잘못된 값을 입력하였습니다. 한 자리 숫자만 입력하세요")    
    
except BigNumberError as err:    
    print("에러가 발생하였습니다. 한 자리 숫자만 입력하세요.")  
    print(err)  

# finally

class BigNumberError(Exception):  
    def __init__(self, msg):  
        self.msg = msg  

    def __str__(self):  
        return self.msg  
  
try:    
    print("한 자리 숫자 나누기 전용 계산기입니다.")    
    num1 = int(input("첫 번째 숫자를 입력하세요 : "))    
    num2 = int(input("두 번째 숫자를 입력하세요 : "))    
    if num1 >= 10 or num2 >= 10:    
        raise BigNumberError("입력값 : {0}, {1}".format(num1, num2))    
    print("{0} / {1} = {2}".format(num1, num2, int(num1 / num2)))    
    
except ValueError:    
    print("잘못된 값을 입력하였습니다. 한 자리 숫자만 입력하세요")    
    
except BigNumberError as err:    
    print("에러가 발생하였습니다. 한 자리 숫자만 입력하세요.")  
    print(err)  

finally:    
    print("계산기를 이용해 주셔서 감사합니다.")    


# 모듈  

import theater_module  
theater_module.price(3) #3명이서 영화보러 갔을 때 가격  
theater_module.price_morning(4)  
theater_module.price_soldier(8)  

import theater_module as mv  
mv.price(3)  
mv.price_morning(4)  
mv.price_soldier(5)  
  
from theater_module import *  
price(3)  
price_morning(4)  
price_soldier(5)  
  
from theater_module import price, price_morning  
price(3)  
price_morning(5)  

from theater_module import price_soldier as price  
price(5)  


```python
#일반 가격
def price(people):
    print("{0}명 가격은 {1}원 입니다.".format(people, people*10000))


#조조할인 가격
def price_morning(people):
    print("{0}명 조조할인 가격은 {1}원 입니다.".format(people, people*6000))


#군인할인 가격
def price_soldier(people):
    print("{0}명 군인 가격은 {1}원 입니다.".format(people, people*4000))
```


# 패키지(모듈의 집합)
```python
# from travel.thailand import ThailandPackage
# trip_to = ThailandPackage()
# trip_to.detail()

# from random import *
from travel import *
trip_to = vietnam.VietnamPackage()
trip_to = thailand.ThailandPackage()

trip_to.detail()
```

__init__.py
```python
__all__ = ["vietnam", "thailand"]
```
