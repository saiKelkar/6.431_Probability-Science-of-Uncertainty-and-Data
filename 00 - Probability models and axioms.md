
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
- de Morgan's laws
  $$(S \cup T)^c = S^c \cap T^c$$
  $$(S \cap T)^c = S^c \cup T^c$$

**Probabilistic Models** -- a mathematical description of an uncertain situation
Elements:
- sample space $\Omega$, which is the set of all possible outcomes of an experiment
- probability law, which assigns to a set A of possible outcomes (also called an event) a non-negative number P(A) (called the probability of A) that encodes our knowledge or belief about the collective likelihood of the elements of A![[Screenshot_2026-04-22_12-19-32.png]]
**Sample Space and Events** -- subset of the sample space, that is the collection of possible outcomes is called an event

**Choosing an Appropriate Sample Space** -- 
- Mutually Exclusive (No Overlap rule): different elements of the sample space should be distinct and mutually exclusive so that when the experiment is carried out, there is a unique outcome
  For e.g., if the bins are labelled {1 or 3} and {1 or 4}
  if we roll the die and get a 1, we are stuck. does the outcome belong in the first bin or the second? it fits both
  
- Collectively Exhaustive (No Gaps rule): sample space must cover every single possibility
  For e.g., if we are rolling a standard six-sided die, but the sample space is S = {1, 2, 3, 4, 5}
  if we roll a 6, our model breaks because that outcome doesn't exist in the universe

- Goldilocks Level of Detail: we need enough detail to answer our specific question, but not so much that the model becomes impossible to calculate
  For e.g., we are tossing a coin to see if we win a bet
  low detail (just right): S = {H, T} <-- perfect for our needs
  high detail (too much): S = {H and landed at 2:01 PM, H and landed at 2:02 PM,...} <-- irrelevant detail that adds clutter to the math

**Sequential Models** -- a way to map out experiments that happen in steps rather than all at once
For e.g., when we toss a coin three times, we don't just get a result but we get a sequence. 
- Tree Structure: most common way to visualize
  Nodes (the dots) -- represent a point in time where you are standing and waiting for something to happen
  Branches (the lines) -- represent the possible outcomes of the next step
  Leaves (the ends) -- each final path from the root to the tip of the branch represents exactly one unique outcome in your sample space ($\Omega$)
  
  Tree diagram ensures that our sample space is mutually exclusive and collectively exhaustive
  - Mutually Exclusive: We can only follow one path from the root to a leaf
  - Collectively Exhaustive: If we've drawn all the branches correctly, there is no way to finish the experiment without ending up at one of the leaves. 
![[Screenshot_2026-04-22_14-18-42.png]]

**Probability Laws** -- this specifies the likelihood of any outcome, or of any set of possible outcomes (an event)
Probability law assigns to every event A, a number P(A), called the probability of A, satisfying the following axioms:
- P(A) ≥ 0, for every A
- If A and B are two disjoint events, then the probability of their union satisfies
  $P(A \cup B) = P(A) + P(B)$ 
- The probability of the entire sample space $\Omega$ is equal to 1, that is, P($\Omega$) = 1

**Discrete Models** -- (countable logic)
if the sample space consists of a finite number of possible outcomes, then the probability law is specified by the probabilities of the events that consist of a single element. 
In particular, the probability of any event $\{s_1, s_2, \dots,s_n\}$ is the sum of the probabilities of its elements:
$$P(\{s_1, s_2, \dots,s_n\}) = P(\{s_1\}) + P(\{s_2\}) + \dots + P(\{s_n\})$$

**Discrete Uniform Probability Law** -- if the sample space consists of n possible outcomes which are equally likely (i.e., all single element events have the same probability), then the probability of any event A is given by
$$P(A) = \frac{\text {Number of elements of A}}{n}$$

**Continuous Models** -- (area logic)
probabilities of a single element events may not be sufficient to characterize the probability law.
the sample space $\Omega$ is an interval (like \[0, 1]) or a 2D / 3D region. We can no longer count the points because there are infinite number of points between any two values. 

The probability of a single-element event (a specific point) is 0 -- if a single point had a tiny positive probability, say 0.0001, then adding up the infinite points in the interval would result in a total probability of infinity, which violates the rule that the total must be 1

So instead of counting, we use measure,
$$P(A) = \frac{\text{Area of A}}{\text{Total Area of }\Omega}$$

**Properties of Probability Laws** -- 
- if $A \subset B$, then P(A) ≤ P(B)
- $P(A \cup B)$ = P(A) + P(B) - $P(A \cap B)$ 
- $P(A \cup B)$ ≤ P(A) + P(B)
- $P(A \cup B \cup C)$ = P(A) + $P(A^c \cap B)$ + $P(A^c \cap B^c \cap C)$ ![[Screenshot_2026-04-25_13-00-47.png]]

**Conditional Probability** -- 