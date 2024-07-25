String pattern matching
- Given a String(T), find a substring that matches the pattern (P)
- Run time: O(nm)

Boyer-Moore
- Run time: O(nm + s)
	- n is the length of the text
	- m is the length of the pattern
	- s is the size of the (alphabet)
		- all characters in either T or P
- Looking-glass heuristic:
	- compare right to left
- Character-jump heuritic
	- if the mismatch occurs at the element T[i] = c, align the last occurrence of c in P with T[i] or shift P until you move past the bad character (align P[0] with T[i + 1]) -> shift it one character after the mismatch
	- if c is in p and its last occurrence is c', then there is no way we can have a match when c is overlapping with chars after c'
	- ![[Pasted image 20231010121711.png]]
	- literally go left to right and look for matching characters at the last character
- Last occurrence function
	- Map the set of letters to the largest index where P[i] = c
	- Example:
		- chars = {a, b, c, d}
		- Pattern = cabaab
		- last occured: a(4), b(5), c(0), d(-1)
- Special occurrence where you shift one tot he right

- Knuth-Morris-Pratt Algorithm (KMP)
	- Optimal Run Time: O(m + n)
	- Compares String left to right
		- but shift string as far as possible
- Failure Function
	- Preprocess pattern
	- ![[Pasted image 20231010122932.png]]
	- ![[Pasted image 20231010123100.png]]
	- mismatch failure function (a) with the mismatch

Tries
- Ordered tree for a set of strings S
- Node (except root)
	- Has a character
- Children of a Node
	- Alphabetically ordered
- Path from Root to external node
	- Create a string S
- Analysis
	- n: total size of strings in S
	- m: size of string parameter
	- d: size of the alphabet
	- Space usage: O(n)
	- Searches/Insertions/Deletions: O(dm)
- Compressed Tries
	- Maximum number of nodes in a compressed trie storing s words:
		- 2s - 1

Suffix arrays
- T = banana$

#TuteSheet 
Questions 1, 2, 3
Questions 9, 10
Questions 4, 5
Questions 6, 7, 8

Question 1:
```
|   a  | 0 | 1 | 2 | 3 | 4 | 5 | 6 |
| P[j] | K | O | K | K | O | L | A |
| f(j) | 0 | 0 | 1 | 1 | 2 | 0 | 0 |
```

Question 2:
KOKKO KOLA KOKKOLA
KOKKO**L**A

Look at f(j) one before the failure of P[j] so since f(5) == L the start of the next iteration is P[5] == 2

KOKKO KOLAㅤKOKKOLA
ㅤㅤKO**K**KOLA

KOKKO KOLA KOKKOLA
ㅤㅤㅤ**K**OKKOLA

KOKKO KOLA KOKKOLA
ㅤㅤㅤ KO**K**KOLA

KOKKO KOLA KOKKOLA
ㅤㅤㅤ   **K**OKKOLA

...shift by one until...

KOKKO KOLA *KOKKOLA
ㅤㅤㅤ      KOKKOLA*

Question 3:
LAWS OF AVIATION
**A**TIO
 A**T**IO
  **A**TIO
   **A**TIO
shift right by on until...
LAWS OF AVI*ATIO*N
ㅤㅤㅤㅤㅤㅤ *ATIO*

```
| chars| A | T | I | O | L | W | S |
| last | 0 | 1 | 2 | 3 | -1| -1| -1|

Comparing ATIOLWS to ATIO
```

LAWS OF AVI*A*TION
ATI**O**
ㅤㅤ ATI**O**
ㅤㅤㅤㅤㅤ*A*TI**O**
ㅤㅤㅤㅤㅤㅤㅤATIOㅤㅤㅤㅤㅤㅤㅤ

Question 9:
0:  abracadabrarad$
1:  bracadabrarad$
2:  racadabrarad$
3:  acadabrarad$
4:  cadabrarad$
5:  adabrarad$
6:  dabrarad$
7:  abrarad$
8:  brarad$
9:  rarad$
10: arad$
11: rad$
12: ad$
13: d$
14: $

14: $
0:  abracadabrarad$
7:  abrarad$
3:  acadabrarad$
12: ad$
5:  adabrarad$
10: arad$
1:  bracadabrarad$
8:  brarad$
4:  cadabrarad$
13: d$.
6:  dabrarad$
2:  racadabrarad$
11: rad$
9:  rarad$

Qeustion 10:
```
| I  | 0  | 1  | 2  | 3  | 4  | 5  | 6  | 7  | 8  | 9  | 10 | 11 | 12 | 13 | 14 |
| T  | a  | b  | r  | a  | c  | a  | d  | a  | b  | r  | a  | r  | a  | d  | $  |
| SA | 14 | 0  | 7  | 3  | 12 | 5  | 10 | 1  | 8  | 4  | 13 | 6  | 2  | 11 | 9  |
```

string i occurs at
i = 11, i = 2, i = 9