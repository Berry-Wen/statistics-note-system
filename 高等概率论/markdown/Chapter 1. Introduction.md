## Chapter 1. Introduction

**Introduction**

**Random Experiments**

1. Output can not be surely predicted in advance;
2. When one repeats the same experiment a large number of times one can observe some "regularity" in the average output

**The state space**

This is the set of all possible outcomes of the experiment, and it is usually denoted by $\Omega$ 

**The events**

An "event" is a property which can be observed either to hold or not to hold after the experiment is done.

In mathematical terms, an event is a subset of $\Omega$. If $A$ and $B$ are two events, then,

+ the contrary event is interpreted as the complement set $A^C$ 
+ the event " $A$ or $B$ " is interpreted as the union $A \cup B$
+ the event " $A$ and $B$ " is interpreted as the intersection  $A \cap B$ 
+ the sure event is $\Omega$ 
+ an **elementary event** is a "singleton"

  + i.e. a subset $\left\{  \omega\right\}$ containing a single outcome $\omega$ of $\Omega$ 


+  $\mathcal{A}$: the family of all events.
+  $2^{\Omega}$ :the set of all subsets of $\Omega$ 

-------------------

The family $\mathcal{A}$ should be "stable" by the logical operations described above: 

----------------------

   If $A,B \in \mathcal{A}$ , then we must have
$$
   A^{C} \in \mathcal{A}, \qquad A \cap B \in \mathcal{A}, \qquad A \cup B \in \mathcal{A}
$$

   and also
$$
   \Omega \in \mathcal{A} \quad and \quad \emptyset \in \mathcal{A}
$$

----------------------

**The probability**

With each event $A$ one associates a number denoted by $P(A)$ and called the "probability of A"

This number measures the likelihood of the event $A$ to be realized a **priori** , before performing the experiment. It is chosen between 0 and 1, and the most likely the event is, the closer to 1 this number is.

To get an idea of the properties of these numbers, one can imagine that they the limits of the "frequency" with which the events are realized:

Let us repeat the same experiment $n$ times; the $n$ outcomes might of course be different (think of $n$ successive tosses of the same dice, for instance). Denote by $f_n(A)$ the frequency with which the event $A$ is realized (i.e. the number of times the event occurs, divided bu $n$)

Intuitively we have:
$$
P(A) = \lim_{n \to \infty} f_n(A)
$$

Form the obvious properties of frequencies, we immediately deduce that:

1. $0 \le P(A) \le 1$ 
2. $P(\Omega)=1$ 
3. $P(A \cup B) = P(A) +P(B) \quad if \quad A \cap B = \emptyset$

A mathematical model for our experiment is thus a triple  $(\Omega,\mathcal{A},P)$ , consisting of

+ the space $\Omega$ 
+ the family $\mathcal{A}$ of all events
+ the family of all $P(A)$ for $A \in \mathcal{A}$ 

Hence we can consider that $P$ is a map from $\mathcal{A}$ into $[0,1]$ , which satisfies at least the properties (2) and (3) above (plus in fact an additional property, more difficult to understand, which will be given in the next Chapter)

**Random variable**

A random variable is a quantity which depends on the outcome of the experiment.

In mathematical terms, this is a map from $\Omega$ into a space $E$ ,where often

$$
E = \mathbb{R} \quad or \quad E = \mathbb{R}^{d}
$$

Let $\mathcal{X}$ be such a random variable, mapping $\Omega$ into $E$ . One can then transport" the probabilistic structure onto the target space $E$ , by setting 
$$
P^{\mathcal{X}} (B) = P \left( X^{-1} (B) \right) \quad for \quad B \subset E
$$

Where $\mathcal{X}^{-1}(B)$ denotes the pre-image of $B$ by $\mathcal{X}$ 

- i.e. the set of all $\omega \in \Omega$ such that $X(\omega) \in B$ 

This formula defines a new probability, denoted by $P^{\mathcal{X}}$ , but on the space $E$ instead of $\Omega$ . This probability $P^{\mathcal{X}}$ is called the **law of the variable** $\mathcal{X}$ 

<br />
<br />

**Example** (toss of two dice)

We have seen that $\Omega = \left\{ (i,j):1 \le i,j \le 6 \right\}$ , and it is natural to take here $\mathcal{A}=2^{\Omega}$ and

$$
P(A) = \frac{\sharp (A)}{36} \quad if \quad A \subset \Omega
$$

Where  $\sharp(A)$ denotes the number of points in $A$ 

One easily verifies the properties (1),(2),(3) above, and 
$$
P \left( \left\{ \omega \right\} \right) = \frac{1}{36}
$$

for each singleton

The map $X:\Omega \to \mathbb{N}$ defined by
$$
X(i,j) = i+j
$$
is the random variable "sum of the two dices" , and its law is 
$$
P^{\mathcal{X}}(B) = \frac{ \text{number of pairs $(i,j)$ such that $i+j \in B$} }{36}
$$
(for example, $P^{\mathcal{X}} \left( \left\{ 2 \right\} \right) =P \left( \left\{ 1,1 \right\} \right)=\frac{1}{36}$, $P^{\mathcal{X}} \left( \left\{ 3 \right\} \right)=\frac{2}{36}$, etc ...)

