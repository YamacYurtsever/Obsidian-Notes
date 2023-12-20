- A concept in computer science that measures the amount of time an algorithm takes to complete as a mathematical function of the size of its input
- It helps us understand how the algorithm's performance scales with the size of the input

### Asymptotic Notation
- **O(i) : Big O Notation**
Maximum n. of steps to finish the algorithm (Worst Case)
- **Ω(i) : Big Omega Notation**
Minimum n. of steps to finish the algorithm (Best Case)
- **Θ(i) : Big Theta Notation**
When O(i) is equal to Ω(i)

### Common Runtimes
! Ordered in increasing time complexity
1. **O(1) : Constant Time**
	- The running time of the algorithm remains constant, regardless of the size of the input. 
	- E.g.: Accessing an element in an array by index
2. **O(log n): Logarithmic Time** ^fd9f43
	- The running time grows logarithmically with the size of the input
	- E.g.: [[Search Algorithms#Binary Search | Binary Search]]
	- ! Usually when something is being divided into multiple parts, the running time is logarithmic
1. **O(n): Linear Time**
	- The running time is directly proportional to the size of the input
	- E.g.: [[Search Algorithms#Linear Search | Linear Search]]
2. **O(n log n): Linearithmic Time**
	- E.g.: [[Sort Algorithms#Merge Sort | Merge Sort]]
3. **O(${n^k}$): Polynomial Time**
	- The running time is a polynomial function of the input size
	- [[Sort Algorithms#Selection Sort | Selection Sort]] & [[Sort Algorithms#Bubble Sort | Bubble Sort]]
4. **O(2^n): Exponential Time**
	- The running time grows exponentially with the size of the input
	- E.g.:  [[Recursion | Recursive]] Fibonacci
![[Recursion#^fa4b58]]
7. **O(n!): Factorial Time**
	- The running time grows factorially with the size of the input
	- E.g.: Brute-Force Search for TSP


