# Matrix mulptiplication problem
Implementation using dynamic programming and comparsion with brute force method.

There are only result. You can find other staff in paper(ADD LINK).

## Brute Force
Pseudo-code for brute force. 'sizes' - std::vector of integers with sizes of matrixes.

```
1. 	seqSize = sizes.length – 2
2. 	result = +∞
3. 	for i = 1..seqSize
4. 	seq[i] = i+1
5. 	do
6. 		seq = PERMUTATION(seq)
7. 		for i = 0..seqSize
8. 			left = seq[j] – 1
9. 			while (seq[left] == 0)
10. 			left = left - 1;
11. 		right = seq[j] + 1
12. 		while (seq[left] == 0)
13. 			right = right + 1;
14. 		temp = temp + seq[left] * seq[i] * seq[right]
15. 		sizes[ seq[j] ] = 0
16. 		if ( temp < result )
17. 			solution = seq
18. while(NEXT_PERMUTATION(seq))
19. RETURN solution 
```
$C_{BF}^M (N)∈O(N)$ - Memory difficulty of brute force method.

$C_{BF}^T (N)∈O(N*N!)$ - Time difficulty of brute force.

$C_{BF}^M (N)=2*(N-1)!*(N-1)$ - amount of Operations for brute force.

## Dynamic Programming
Pseudo-code:

```
1. n = sizeMatrix.length
```

$C_{DP}^M (N)∈O(N^2)$ - Memory difficulty of DP method.

$C_{DP}^T (N)∈O(N^3)$ - Time difficulty of DP method.

$C_DP^O (N)∈O(N^2)$ - amount of Operations for DP method.

### Amount of multiplications for algorithms

![Imgur](http://i.imgur.com/J14VZgo.png)

### Comparsion of time by two algorithmss
Circles and squares mean tested time, doted lines theretical estimation.

![Imgur](http://i.imgur.com/PPsUKnP.png)