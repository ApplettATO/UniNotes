4.1
method LinearSearch2(a: array, P: T -> bool) returns (n: int)
	ensures -1 <= n <= a.Length
	ensures n == -1 || P(a[n])
	ensures n == -1 ==> forall i :: 0 <= i < a.Length ==> !P(a[i])
	ensures n != -1 ==> forall i :: 0 <= I < n ==> !P(a[i])
{
	n := 0;
	while n != a.Length
	{
		if (P(a[n])) { return; }
		n := n + 1;
	}
	n := -1;
}