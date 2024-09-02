 To malloc a string of characters, we need to multiply the number of bytes of a char by the number of chars we need in our string, without forgetting to add an extra char for the final `\0`.
```
char *cpy; char str[7] = "Hello!"; 
// Let's say we want to malloc enough space to make a copy of str. We need to multiply the size of a char by the length of str, +1 for the final \0. 
// [H][e][l][l][o][!][\0] = 6 char + 1 char 
cpy = malloc(sizeof *cpy * (strlen(str) + 1));
```
Finally, to allocate an array of strings, we must first allocate the array itself, and each individual string afterwards.
```
char **strs; 
// We malloc the array. Let's say we want 3 strings in our array: 
strs = malloc(sizeof *strs * (3 + 1)); // +1 for the last \0 
// Then we can malloc each string (in practice, we would probably do this in a loop): 
strs[0] = malloc(sizeof **strs * (5 + 1)); // +1 for the final \0 
strs[1] = malloc(sizeof **strs * (5 + 1)); 
strs[2] = malloc(sizeof **strs * (1 + 1)); 
strs[3] = malloc(sizeof **strs * 1); 
/* To visualize our currently empy array, let's fill it with some characters. It will look something like this: 
	[H][e][l][l][o][\0] 
	[w][o][r][l][d][\0] 
	[!][\0] 
	[\0] 
*/
```
