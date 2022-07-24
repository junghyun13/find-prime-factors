# find-prime-factors
# python
# Find prime factors Enter the desired number in N, enter the desired number, and check the number of prime factors and how many are printed! 소인수 찾아보기 N에 원하는 개수를 입력하고 원하는 수를 입력한후 그 수의 소인수 값과 몇개가 출력되어는지를 확인해보자!
N=int(input())
for i in range(N):
    num=int(input())
    a=2
    cnt=[]
    while a<=num:  #a가 num이 될때까지 반복
        if num%a==0:
            num//=a 
            cnt.append(a) 
        else:
            a+=1  #num이 a로 나누어지지 않으면 a를 늘린다.
    cnt.sort()  #cnt라는 리스트안에 있는 숫자를 작은순으로 정리
    test=set(cnt)  #set함수를 이용해서 어떤인수가 나왔는지를 확인
    value=sorted(list(test))  
    for i in range(len(value)): 
        print(value[i],cnt.count(value[i]))  #소인수,나온 소인수의 개수
#input--> 2  6  24
#result--> 6입력후 2 1  3 1  24입력후 2 3  3 1
