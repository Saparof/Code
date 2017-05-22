# Code for Codeforces
a = input().split()
n = int(a[0])
m = int(a[1])
k = int(a[2])
ans = n-1
A = input().split()
for i in range(n-m):
  x = int(A[i+m])
  if x!=0 and x<=k:
    ans = i+1
    break
for i in range(m-1):
  x = int(A[m-2-i])
  if x!=0 and x<=k:
    ans = min(ans,i+1)
    break

print(ans*10)
