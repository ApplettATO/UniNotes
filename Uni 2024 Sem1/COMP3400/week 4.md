let n = 1
- max regions = 2
- min regions = 2
- possibilities = 1
let n = 2
- max regions = 4
- min regions = 3
- possibilities = 2
let n = 3
- max regions = 6
- min regions = 4
- possibilities = 3
for any n
- max regions = 2n
- min regions = n + 1
- possibilities = n

Assume P(n), that for any number n, that all adjacent regions can be coloured a different colour

consider n + 1 chords 

All horses are the same colour
- can you assume that sets {1, ... n} and {2, ..., n+1} are the same colour


Prac Answers
P === For every placement of n chords on a circle, there is a correct colouring.

Base case P(0): () is correctly coloured

Suppose P(n) is true, show P(n+1) is true
Take some placement of n+1 chords on a circle. After deleting some chord C, we have a circle with n chords. Supposition => there is some valid colouring

Add back C. Notice any edge along which our colouring fails lies on C.
Invert every colour, above the line (or to the left). Now one side of each problem edge has been inverted. Because it was previously a problem (i.e. the same), now it is no longer a problem (i.e. different colouring).

Note that there are no new problems. Why? The inversion of any valid colouring is valid. Thus our colouring is valid => P(n+1)