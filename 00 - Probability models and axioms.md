
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

**Conditional Probability** -- this provides us with a way to reason about the outcome of an experiment based on partial information
this takes into account the knowledge for any event A, gives us the conditional probability of A given B, denoted by $P(A \mid B)$ 

$$P(A \mid B) = \frac{\text {number of elements of }A \cap B}{\text {number of elements of B}}$$

$$P(A \mid B) = \frac {P(A \cap B)}{P(B)}$$

where we assume that P(B) > 0

**Properties of Conditional Probability** -- 
- conditional probability of an event A, given an event B with P(B) > 0, is defined by $$P(A \mid B) = \frac {P(A \cap B)}{P(B)}$$
  all known properties of probability laws remain valid for conditional probability laws
- conditional probabilities can also be viewed as a probability law on a new universe B, because all of the conditional probability is concentrated on B
- in the case where the possible outcomes are finitely many and equally likely, we have $$P(A \mid B) = \frac{\text {number of elements of }A \cap B}{\text {number of elements of B}}$$

**Total Probability Theorem and Bayes' Rule** -- to find the big answer, look at every possible scenario, calculate its contribution, and add them up

(core concept - partition): 
imagine designing a floor plan for a building, we divide the total area into three distinct zones - residential, commercial, and public
- these zones are disjoint (they don't overlap)
- together, they form a partition (they cover the whole floor)

these zones are our events $A_1, A_2, A_3, \dots, A_n$
now if we want to find the total probability of a specific event B (e.g., the light bulb is broken), then we look at the risk in each zone individually
$$P(B) = P(A_1)P(B \mid A_1) + P(A_2)P(B \mid A_2) + \dots + P(A_n)P(B \mid A_n)$$
e.g., we are playing a game, and our chance of winning depends entirely on who we are playing against

identifying scenarios: 
type 1 (half of the players): $P(A_1)$ = 0.5 (Easy mode)
type 2 (quarter of the players): $P(A_2)$ = 0.25 (Medium mode)
type 3 (quarter of the players): $P(A_3)$ = 0.25 (Hard mode)

win rates:
if we play type 1, we win 30% of the times: 0.3
if we play type 2, we win 40% of the times: 0.4
if we play type 3, we win 50% of the times: 0.5

total win probability:
(0.5 x 0.3) + (0.25 + 0.4) + (0.25 x 0.5) = 0.375 = 37.5%

**Bayes' Rule** -- it's about the math of updating your beliefs based on new evidence
- the cause $(A_i)$: these are the different scenarios (e.g., opponent type 1, 2, or 3)
- the effect (B): this is the outcome we observed (e.g., "I won the game" or "The radar beeped")
the formula asks: given that effect B happened, what is the probability that cause $A_i$ was the reason?
$$P(A_i \mid B) = \frac{P(A_i)P(B \mid A_i)}{P(B)}$$
where P(B) != 0

e.g., radar is 99% accurate at detecting a plane if it's there. But planes are only there 5% of the time
the radar goes off (B happens)
is there actually a plane (A)?

even though it's 99% accurate, the 34.26% result seems low; because planes are so rare (5%), the false alarms from the other 95% of the time (where the radar has a 10% error rate) actually outnumber the true detection
--> always look at the prior probability (P(A)). if something is very rare, even a positive test result might still mean it's unlikely

**Independence** -- two events are independent if knowing that one happened tells us absolutely nothing about the other

two events A and B are independent if and only if:
$$P(A \cap B) = P(A) \cdot P(B)$$
alternatively, if P(B) > 0:
$$P(A \mid B) = P(A)$$
the second version: "the probability of A given that I already know B, is exactly the same as the original probability of A. the knowledge of B didn't change my mind"

independence != disjoint
disjoint (mutually exclusive): events A and B cannot happen at the same time $(A \cap B) = \emptyset$ 
independence: events A and B don't affect each other

crucial logic: if two events are disjoint, they are highly dependent. if I tell you that A happened, you know with 100% certainty that B did not happen. therefore, they cannot be independent.

**Conditional Independence** -- (the context rule)
two events can be independent in general, but become dependent once you have extra information (event C). Or, they can be dependent normally, but become independent once C is known

e.g., two biased coins
imagine having a blue coin (99% heads) and a red coin (1% heads)
- without knowing which coin you picked, if the first toss is Heads, you immediately suspect you have a Blue coin. this makes you bet that the second toss will also be heads. in this case toss 1 and toss 2 are dependent
- once you know which coin you picked (condition C) -- if someone tells us "you definitely have the blue coin", then the first toss tells us nothing about the second. the bias is already a known constant. the tosses are conditionally independent. 

**Mutual Independence** -- (all or nothing rule)
for a collection of events (like $A_1, A_2, A_3$) to be truly independent, two things must be true:
- pairwise independence: $A_1, A_2$ are independent, $A_2, A_3$ are independent, and $A_1, A_3$ are independent
- the full group condition: the probability of all three happening together must equal the product of their individual probabilities
  $P(A_1 \cap A_2 \cap A_3) = P(A_1)P(A_2)P(A_3)$ 

**Reliability** -- (series vs parallel)

series connection (the weak link logic):
success rule - all components must work
math - multiply the probabilities
P(series subsystem succeeds) = $p_1p_2...p_m$ 
consequence - the more components you add in series, the lower the total reliability

parallel connection (the redundancy logic):
success - at least one component must work
math - it's easier to calculate the chance of total failure and subtract from 1
P(parallel subsystem succeeds) = 1 - P(parallel subsystem fails)
							 = 1 - (1 - $p_1$)(1 - $p_2$)...(1 - $p_m$)
consequence - adding components in parallel increases reliability
![[Screenshot_2026-04-26_10-50-25.png]]
subsystem: C -> B through E or F are parallel parts
main line: once subsystem is known, we treat it as a single series block with node A
final aggregate: we end up with two main parallel path from A to B (from A -> C (including subsystems) -> B and A -> D -> B)

**Independent Trials and the Binomial Probabilities** -- 