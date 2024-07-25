J && !B

3.1)
a)
x := 0;
while x != 100
	invariant true
assert x == 100;

initial proof obligation: yes
assertion: yes

{x == 100 && true}
{x == 100}


b)
x := 20;
while 10 < x
	invariant x%2 == 0
**{10 >= x && x % 2 == 0}**
assert x == 10;

initial proof obligation: yes
assertion: no

c)
x := 20; 
while x < 20 
	invariant x%2 == 0 
**{x >= 20 && x % 2 == 0}**
assert x == 20;

initial proof obligation: yes
assertion: no

d)
x := 3; 
while x < 2 
	invariant x%2 == 0 
**{x >= 2 && x%2 == 0}**
assert x%2 == 0;

initial proof obligation: no
assertion: yes

e)
x := 0; 
while x < 100 
	invariant 0 <= x < 100 
**{x >= 100 && 0 <= x < 100}**
**false** -> can prove anything after false :. assertion -> yes
assert x == 25;

initial proof obligation: yes
assertion: yes

3.3)
a)
x := 0; 
while x < 100 
	**invariant 0 <= x <= 102** -> **x%3 == 0 && x <= 102**
	*{x >= 100 && 0 <= x <= 102}*
{
	x := x + 3;
} 
assert x == 102;

3.4)
method UpWhileLess(N: int) returns (i: int) 
	requires N >= 0 
	ensures i == N 
{ 
	i := 0; 
	while i < N 
		invariant i <= N
		decreases N - i
	{ 
		i := i + 1; 
	} 
}

method UpWhileNotEqual(N: int) returns (i: int) 
	requires N >= 0 
	ensures i == N 
{ 
	i := 0; 
	while i != N 
		invariant i <= N
		decreases N - i
	{ 
		i := i + 1; 
	}
}

method DownWhileNotEqual(N: int) returns (i: int) 
	requires N >= 0 
	ensures i == 0 
{ 
	i := N; 
	while i != 0 
		invariant i >= 0
		decreases i
	{ 
		i := i - 1; 
	}
}

method DownWhileGreater(N: int) returns (i: int) 
	requires N >= 0 
	ensures i == 0 
{ 
	i := N; 
	while i > 0 
		invariant i >= 0
		decreases i
	{ 
		i := i - 1; 
	} 
}

3.5)
Let Power be defined as

ghost function Power(n: nat): nat { 
	if n == 0 then 1 else 2^Power(n - 1) 
} 

and ComputePower be the method method 

ComputePower(N: int) returns (y: nat) 
	requires N >= 0 
	ensures y == Power(N) 
{ 
	y := 1; 
	var x := 0; 
	while x != N 
		invariant 0 <= x <= N 
		invariant y == Power(x) 
		{ 
			x, y := x + 1, y + y; 
		} 
	}

{x == N && 0 <= x <= N && y == Power(x)}
{x == N && y == Power(x)} strengthening
{y == Power(N)}