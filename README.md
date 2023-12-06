[![Open in Visual Studio Code](https://classroom.github.com/assets/open-in-vscode-718a45dd9cf7e7f842a935f5ebbe5719a5e09af4491e668f4dbf3b35d5cca122.svg)](https://classroom.github.com/online_ide?assignment_repo_id=12078474&assignment_repo_type=AssignmentRepo)
# Asymptotic Equivalences

In the lectures, we said that logarithms with different bases don't affect the
asymptotic complexity of an algorithm. Prove that $O(\log_{2} n)$ is the same as
$O(\log_{5} n)$. Use the mathematical definition of $O$ -- do a formal proof,
not just the intuition.

I have started with the formal definition of $O$ below. Add your answer to this
markdown file. [This
page](https://docs.github.com/en/get-started/writing-on-github/working-with-advanced-formatting/writing-mathematical-expressions)
might help with the notation for mathematical expressions.

$T(n) \in O(f(n)) \iff \exists c, n_0: T(n) \leq c \cdot f(n) \forall n \geq n_0$

If we combine this formal definition with the basic rules of logarithms, we can show this formally. 

Specifically, we know $\exists c, n_0: f(n) \leq log_2n$ while $n\geq n_0$. Another thing to consider is that $log_2n = c$, which is the same as $2c = n$. The same can be said about $log_5n = c’ = 5c’ = n$. If $f(n) = log_2n$, then $g(n) = c \cdot f(n)$. Now, $\forall x \in O(log_2n)$ and $x \in O(log_5n)$ and $\forall y \in O(log_2n)$, $y \in O(log_5n)$. This means they are **subsets** of each other. 
The log base change rule states ${log_{10}n / log_{10}2} = log_2n$. If we make $c = log_{10}n / log_{10} 2$ then we can rearange to $c/log_{10}2 = log_{10} n$ then conclude that $f(n) \in g(n)$ and thus $log_2n \in O(log_{10}n)$.

I also found a different way to look at it using the base change rule. If we make $c = 1/log_{10} 2$ then we can conclude that $f(n) \in g(n)$ and thus $log_2n \in O(log_{10}n)$ since $log_{2}n / log_2. Then we do the exact opposite to prove the other way. 

Intuitivly, as n approaches ∞, things like exponents and factorials are going to take control and constants are not going to make much difference whatsoever, which is why we get rid of them.

**Log bases are nothing but constants.**


Sources:

https://xlinux.nist.gov/dads/HTML/bigOnotation.html

https://math.stackexchange.com/questions/620145/understanding-definition-of-big-o-notation

https://en.wikipedia.org/wiki/BigjhN34O_notation#Formal_definition

https://stackoverflow.com/questions/30201391/how-to-write-a-recurrence-relation-for-a-given-piece-of-code

https://mathinsight.org/logarithm_basics

https://www.quora.com/Why-we-do-not-consider-base-of-log-in-time-complexity

https://www.rapidtables.com/math/algebra/Logarithm.html

https://www.cuemath.com/change-of-base-formula/

Lars Kotthoff, Lectures 1-8, 23 Aug 2022 – 15 Sep 2022

Nicholas Matter, Assignment 1, 16 Sep 2022

