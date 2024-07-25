Exercise 1:
T1 followed by T2
R(y) = 20
y = y + 50 = 70
W(y) = 70

R(y) = 70
y = y x 3 = 210
W(y) = 210

T2 followed by T1
R(y) = 20
y = y x 3 = 60
W(y) = 60

R(y) = 60
y = y + 50 = 110
W(y) = 110

part B: 60, overwrites what happens in T1

part C: lost update - the find value has been lost by T1

Exercise 2:
- 1: belong to different T
- 2: Access same item X
- 3: At least 1 write to X

Part A: S3 and S4
In S3, it would make a cycle (conflict serializable)

Exercise 3:
Schedule 2: abort -> dirty read
READ(Y) = 30
READ(Z) = 56
WRITE(Y) = 42
READ(Y) = 42
WRITE(Y) = 50
READ(X) = 80
WRITE(Z) = 64
Delete T1 ???

Schedule 3:
```
READ(X) = 80
READ(Y) = 30 
							    READ(Z) = 56
WRITE(Y) = 110

```

