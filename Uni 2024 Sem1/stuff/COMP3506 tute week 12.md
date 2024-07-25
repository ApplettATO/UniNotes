Text Compression
- Each letter maps to binary code
	- 0 for left child
	- 1 for right child
- Huffman encoding
	- Run time: O(n + d x log(d))
		- n: size of text
		- d: number of distinct characters
		- PQueue implemented through a heap


#TuteSheet 
Question 1
```
| Char | s | l | e | p | n |
| Freq | 5 | 2 | 4 | 1 | 1 |

Total: 13
```

Question 2:
```mermaid
graph TD;
id1((13)) --> id2((s:5));
id1((13)) --> id3((8));
id3((8)) --> id4((e:4));
id3((8)) --> id5((4));
id5((4)) --> id6((l:2));
id5((4)) --> id7((2));
id7((2)) --> id8((p:1));
id7((2)) --> id9((n:1));
```


s: 0, e: 10, l: 110, p: 1110, n: 1111

spell
0 1110 10 110 110

Question 3:
pens

Question 4:
Scheme 2 or 4
