1) s = input().split(" ")
for i in range(0, len(s), 2):
print(s[i], end=' ')

2) s = list(map(int, input().split(" ")))
for i in range(len(s)):
if s[i] % 2 == 0:
print(s[i], end = ' ')

3) s = list(map(int, input().split(" ")))
for i in range(1, len(s)):
if s[i] > s[i-1]:
print(s[i], end = ' ')

4) s = list(map(int, input().split(" ")))
for i in range(1, len(s)):
if s[i] < 0 and s[i-1] < 0 or s[i] > 0 and s[i-1] > 0:
print(s[i-1], s[i])
break

5) s = list(map(int, input().split(" ")))
res = 0
for i in range(1, len(s) - 1):
if s[i] > s[i-1] and s[i] > s[i+1]:
res+=1
print(res)

6) s = list(map(int, input().split(" ")))
maxx = s[0]
ind = 0
for i in range(1, len(s)):
if s[i] > maxx:
maxx = s[i]
ind = i
print(maxx, ind)

7) s = list(map(int, input().split(" ")))
n = int(input())
res = len(s)+1
for i in range(len(s)):
if s[i] < n:
res = i + 1
break
print(res)
   
8) s = list(map(int, input().split(" ")))
res = 1
for i in range(1, len(s)):
if s[i] != s[i-1]:
res+=1
print(res)
   
9) A = [int(x) for x in input().split()]
for i in range(0, len(A) - 1, 2):
[i], A[i + 1] = A[i + 1], A[i]
for i in range(len(A)):
print(A[i], end=' ')
    
10) s = list(map(int, input().split(" ")))
minn = s[0]
maxx = s[0]

for i in range(len(s)):
if s[i] > maxx:
maxx = s[i]
if s[i] < minn:
minn = s[i]
for i in range(len(s)):
if s[i] == maxx:
print(minn, end = ' ')
elif s[i] == minn:
print(maxx, end = ' ')
else:
print(s[i], end = ' ')
    
11) s = list(map(int, input().split(" ")))
k = int(input())
for i in range(len(s)):
if k < i:
s[i-1] = s[i]
s.pop()
for i in range(len(s)):
print(s[i], end = ' ')
    
12) s = list(map(int, input().split(" ")))
k, c = map(int, input().split())

for i in range(len(s)):
if k <= i:
s[i], c = c, s[i]
s.append(c)
for i in range(len(s)):
print(s[i], end = ' ')
    
13) s = list(map(int, input().split(" ")))

res = 0
for i in range(len(s)):
for j in range(i+1, len(s)):
if s[i] == s[j]:
res+=1
print(res)
    
14) s = list(map(int, input().split(" ")))
l = 0
for i in range(len(s)):
for j in range(len(s)):
if s[i] == s[j] and i != j:
l = 1
break
if l == 0:
print(s[i], end = ' ')
l = 0
    
15) n, k = map(int, input().split())
s = ['I']*n
for i in range(k):
l, r = map(int, input().split())
for j in range(l-1, r):
s[j] = '.'
print("".join(s))
    
16) q = []
for i in range(8):
x, y = map(int, input().split())
q.append((x, y))
res = "NO"
for i in range(7):
for j in range(i + 1, 8):
if q[i][0] == q[j][0] or q[i][1] == q[j][1] or abs(q    [i][0] - q[j][0]) == abs(q[i][1] - q[j][1]):
res = "YES"
break
print(res)
