# Problem E
	- For $1 \times n$, let's consider the case when the first element is $0$
	- $0, 1, 0, \cdots => dp[i] = dp[i + 2] + something$
		- 0, 1, 1, 0 [1 will always come after 0, 1,
	- A simple $dp[i, j, bool]$  will suffice.
		- i => length of the array