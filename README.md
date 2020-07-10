# Apple-and-Orange
HackerRank: Apple and Orange



Sam's house has an apple tree and an orange tree that yield an abundance of fruit. In the diagram below, the red region denotes his house, where s is the start point, and t is the endpoint. The apple tree is to the left of his house, and the orange tree is to its right. You can assume the trees are located on a single point, where the apple tree is at point a, and the orange tree is at point b .



When a fruit falls from its tree, it lands d units of distance from its tree of origin along the x-axis. A negative value of d means the fruit fell d units to the tree's left, and a positive value of d means it falls d units to the tree's right.

Given the value of d for m apples and n oranges, determine how many apples and oranges will fall on Sam's house (i.e., in the inclusive range [s,t])?

For example, Sam's house is between s=7 and t=10 . The apple tree is located at a=4 and the orange at b=12 . There are m=3 apples and n=3 oranges. Apples are thrown apples=[2,3,-4] units distance from a, and oranges=[3,-2,-4] units distance. Adding each apple distance to the position of the tree, they land at[4+2,4+3,4+-4]=[6,7,0] . Oranges land at [12+3,12+-2,12+-4]=[15,10,8]. One apple and two oranges land in the inclusive range 7-10 so we print
1
1




//Code

#!/bin/python3


p=0
q=0
st = input().split()

s = int(st[0])

t = int(st[1])

ab = input().split()

a = int(ab[0])

b = int(ab[1])

mn = input().split()

m = int(mn[0])

n = int(mn[1])

apples = list(map(int, input().rstrip().split()))
oranges= list(map(int, input().rstrip().split()))
   
for i in range(len(apples)):
    apples[i]+=a

for i in range(len(oranges)):
    oranges[i]+=b

for i in range(len(apples)):
    if apples[i]>=s and apples[i]<=t:
        p+=1

for i in range(len(oranges)):
    if oranges[i]>=s and oranges[i]<=t:
        q+=1
    
print(p)
print(q)


    

   
