
1 - Sample space and Probability

**Set** -- collection of objects, which are the elements of the set
- S is a set, and $x$ is an element of S, we write $x \in S$ 
- If $x$ is not an element of S, we write $x \notin S$ 
- If a set has no elements, it is called the empty set, written as $\emptyset$  
- If S contains a finite number of elements, we write it as a list of elements: $S = \{x_1, x_2,..., x_n\}$ 
  
  For example, the set of possible outcomes of a die roll is $\{1, 2, 3, 4, 5, 6\}$  
  the set of possible outcomes of a coin toss is $\{H, T\}$
- If S contains infinitely many elements $x_1, x_2,...$, which can be enumerated in a list (so there are as many elements as there are positive integers):
  $S = \{x_1, x_2,...\}$ and we say that S is countably infinite
  
  For example, the set of even integers can be written as $\{0, 2, -2, 4, -4,...\}$
  Alternatively, we can consider the set of all $x$ that have a certain property $P$, denoted by $\{x \mid x \text{ satisfies } P\}$  
  The symbol "$\mid$" is read as "such that" 
- If every element of a set S is also an element of a set T, we say that S is a subset of T, written as $S \subset T$ 
  If $S \subset T$ and $T \subset S$, the two sets are equal, and we write S = T
- Universal set $\Omega$, contains all objects that could conceivably be of interest in a particular context

**Set Operations** -- 
- complement of a set S, with respect to the universe $\Omega$, is the set $\{x \in \Omega \mid x \notin S\}$ of all elements of $\Omega$ that do not belong to S and is denoted by $S^c$ 
  Note: $\Omega ^c = \emptyset$ 
- union of two sets S and T is the set of all elements that belong to S or T (or both), and is denoted by $S \cup T$ 
  $S \cup T = \{x \mid x \in S \text{ or } x \in T\}$ 
- intersection of two sets S and T is the set of all elements that belong to both S and T, denoted by $S \cap T$ 
  $S \cap T = \{x \mid x \in S \text{ and } x \in T\}$ 
- to consider the union or the intersection of several, even infinitely many sets, for e.g., for every positive integer n, we are given a set $S_n$, then
  $$\bigcup_{n=1}^{\infty} S_n = S_1 \cup S_2 \cup \dots = \{x \mid x \in S_n \text{ for some } n\}$$
  $$\bigcap_{n=1}^{\infty} S_n = S_1 \cap S_2 \cap \dots = \{x \mid x \in S_n \text{ for all } n\}$$
- two sets are disjoint if their intersection is empty
- collection of sets is said to be a partition of a set S if the sets in the collection are disjoint and their union is S
- if x and y are two objects, we use $(x, y)$ to denote the ordered pair of x and y
- set of scalars is denoted by $R$ 
- set of pairs of scalars, i.e., the two-dimensional plane (or three-dimensional space) is denoted by $R^2$ or $R^3$ respectively ![[Screenshot_2026-04-22_11-31-42.png]]

**Algebra of Sets** -- 