# Amortized Analysis

## 1. Aggregate analysis

*T(n) is the upperbound of n operations, the amortized cost per operation is T(n)/n* 

**Stack Operations** 

1. push: O(1)
2. Pop : O(1)
3. Multipop: (pop pop)
   1. Worst case for n operations: $ O(n^2) $ , but not right.
   2. We can only pop the number of push times
   3. The amortized cost its O(n)/n = O(1)

**Incrementing a binary counter** 



## 2. Acounting (Banker's) method

*Each operation has a real cost c and an amortized cost cˆ .*

$\sum_{i=1}^{l} \hat{c_i} >= \sum_{i=1}^{l} c_i$ 

**Amortized Cost:** The amount we charge an operation 

(Total amortized cost of n operations = actual cost)

**Credit:**  amortized cost - specific objects in the data structure

**Methodology**

1. Your work is to come up with the amortized costs and to show that they are valid.
2. Show that the amortized costs are valid
3. $\sum_{i=1}^{l} \hat{c_i} <= X$ for some X
4. Conclude that total cost is at most X.

## 3. Potential method

- Let Di be the “state” of the system after the i th operation. 

- Define a potential function Φ(Di) to be the potential associated with state Di . 

- The i th operation has a real cost of ci 

- Define the amortized cost cˆ of the i th operation by i 

  cˆ=c+Φ($D_i$)−Φ($D_{i-1}$ ) 

**Potential function**: Smooth out the difference

**Methodology**

1. Proof Φ($D_n$)>=Φ($D_{0}$ ) 
2. Then $\sum_{i=1}^{l} \hat{c_i} >= \sum_{i=1}^{l} c_i$ 
3. Repeat methods in methods 2

