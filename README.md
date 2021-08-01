# Analysis of Algorithm
by Ahmad Fariz 

Source https://docs.google.com/document/d/1sml7Zoo5FrppPHLfhwm3OvL6Xi23etxUfQ1wXer6YC4/edit?usp=sharing

## Asymptotic Analysis
Analisis para algoritma untuk menentukan batas/framing algoritma pada performa run time

### Objektif:
menghitung running time dari setiap operasi dalam satuan matematika komputasi. Contoh:
* running time operasi 1 = f(n) -> time increasing linearly as n increases
* running time operasi 2 = g(n2) -> time increasing exponentially as n increases

### Kegunaan : 
untuk menyimpulkan running time dibutuhkan untuk eksekusi algoritma pada:
1. best case 	: minimum time required
2. average case	: average time required
3. worst case	: maximum time required

### Sifat:
input bound

### Common Asymptotic Analysis:
1. O notation : upper bound 
2. 𝜴 notation : lower bound
3. 𝜭 notation : upper + lower bounds

### Common notations:
| | | |
| --- | --- | ---- |
| constant | − | Ο(1)|
| logarithmic | − | Ο(log n) |
| linear | − | Ο(n) |
| n log n | − | Ο(n log n) |
| quadratic | − | Ο(n2) |
| cubic | − | Ο(n3) |
| polynomial | − | nΟ(1) |
| exponential | − | 2Ο(n) |

## Big-O notation
Asymptotic analysis untuk menentukan batas atas alias worst case dari performa algoritma.

### Definisi:
untuk sebuah fungsi f(n),
Ο(f(n)) = { g(n) : there exists c > 0 and n0 such that f(n) ≤ c.g(n) for all n > n0. }

### Objektif:
performance analysis pada:
1. time
2. space

### Time Complexity a.k.a runtime analysis of algorithms
#### Dependency:
1. input size
2. number of operations executed

#### Ekspresi time complexity untuk kompleksitas algoritma:
Untuk problem dengan size N:
* Constant time		: “Order 1” O(1)
* Linear time		: “Order N” O(N)
* Quadratic time		: “Order N squared” O(N2)


#### Prosedur umum time complexity analisis:
1. Cari tahu apa inputnya
2. Cari tahu n merepresentasikan apa: size of input atau jumlah operasi
3. hitung jumlah maksimal operasi yang dijalankan algoritma in terms of n
4. Sisakan highest order terms dalam persamaan
5. hapus faktor konstanta

#### Useful properties:
1. Constant Multiplication
if f(n) = c.g(n) 
-> O(f(n)) = O(g(n)); 
c != 0
2. Polynomial Function
if f(n) = a0 + a1.n + a2.n2 + … + am.nm 
-> O(f(n)) = O(nm)
3. Logarithmic Function
if f(n) = logan and g(n) = logbn 
-> O(f(n)) = O(g(n)); 
all log functions grow in the same manner in terms of Big-O
4. Summation  Function
if f(n) = f1(n) + f2(n) + … + fm(n) and fi(n) ⩽ fi+1(n) ∀ i=1, 2, …, m 
-> O(f(n)) = O(max(f1(n), f2(n), ... , fm(n)))

#### Algorithm classification from best-to-worst time complexity performance:
where n = input size and c is positive constant
1. Constant Running Time	: O(1)
* always take the same amount of time to execute, regardless of the input size
* ideal
* rarely achievable
2. A logarithmic algorithm	: O(log n)
* binary search
3. A linear algorithm		: O(n)
* linear search
4. A superlinear algorithm	: O(nlogn)
* heap sort
* merge sort
5. A polynomial algorithm	: O(nc)
* Strassen’s Matrix Multiplication
* Bubble sort
* Selection sort
* Insertion sort
* Bucket sort
6. An exponential algorithm	: O(cn)
* Tower of Hanoi
7. A factorial algorithm		: O(n!)
* Determinant Expansion by Minors
* Brute force Search Algorithm for Traveling Salesman Problem

#### Mathematical Examples of Runtime Analysis
if n = 10:
log(10) = 1;
10 = 10;
10log(10) = 10;
10^2 = 100;
210 = 1024;
10! = 3628800;

if n = 20:
log(20) = 2.996;
20 = 20;
20log(20) = 59.9;
20^2 = 400;
220 = 1048576;
20! = 2.432902e+18;


### Space Complexity a.k.a Memory Footprint Analysis of Algorithms
performance analysis on the memory usage amount of the program.

#### dependency:
1. memory usage corresponding the implementation of program. 
Example:
* recursive implementation > iterative implementation
2. n
* input size
* amount of storage required for each item
Example:
*simple algorithm with a high amount of input size > complex algorithm with less amount of input size

#### Algorithm classification from best-to-worst space complexity performance:
1. Ideal algorithm		: O(1)
* Linear search
* Binary search
* Bubble sort
* Selection sort
* Insertion sort
* Heap sort
* Shell sort
2. Logarithmic algorithm	: O(log n)
* Merge sort
3. Linear algorithm		: O(n)
* Quick sort
4. Sub-linear algorithm		: O(n+k)
* Radix sort

### Space-Time Tradeoff and Efficiency
1. Biasanya space-efficiency dan time-efficiency tercapai pada arah yang berlawanan
2. Titik diantaranya merupakan kombinasi/tradeoff dari keduanya
3. Tugas kita untuk menemukan algoritma dengan:
* less running time
* less requirement of memory space


## References
* Tutorialspoint. Data Structure - Asymptotic Analysis. [Online] https://www.tutorialspoint.com/data_structures_algorithms/asymptotic_analysis.htm 
* Geeks for Geeks. Analysis of Algorithm | Big-O analysis. [Online] https://www.geeksforgeeks.org/analysis-algorithms-big-o-analysis/ 
