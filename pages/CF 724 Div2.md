# Problem E
	- For $1 \times n$, let's consider the case when the first element is $0$
	- $0, 1, 0, \cdots => dp[i] = dp[i + 2] + something$
	  collapsed:: true
		- 0, 1, 1, 0 [1 will always come after 0, 1,
	- A simple $dp[i, j, bool]$  will suffice.
		- i => length of the array
		- j => first element
		- bool => whether this element will is greater than atleast one of its neighbours
		- For example: 
		  $dp[i, j, 1] = dp[i - 1, j - 1, 0] + dp[i - 1, j, 1] + dp[i - 1, j + 1, 1]$
		  $dp[i, j, 0] = dp[i, j - 1, 0]$
	- Now let's consider $2 * n$
		- We'll have to do more book-keeping.