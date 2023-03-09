# sp2n-fundamental-tilting-charaters

You can find a (short and hopefully sweet) Mathematica notebook to compute the Weyl characters for fundamental tilting modules.

This uses the below formula from <a href="https://arxiv.org/abs/2303.04264">https://arxiv.org/abs/2303.04264</a>

References for the recalled background below can also be found in that paper.

# Background

Fix some $n>0$. Let $\mathcal{A}=\mathbb{Z}[q,q^{-1}]$ for a formal parameter $q$. 
We work with the divided power quantum group for $\mathfrak{sp}_{2n}$. 

Fix any field $\mathbb{K}$ and any $\xi\in\mathbb{K}\setminus\{0\}$, we can specialize this quantum algebra to $U_{\xi}(\mathfrak{sp}_{2n})$ by sending $q\mapsto\xi$. We have **no restrictions** on $\mathbb{K}$ or $\xi$.

The quantum group $U_{\xi}(\mathfrak{sp}_{2n})$ has four types of natural modules, all of which are indexed by dominant integral weights $\lambda\in X^{+}$:

- The **Weyl modules** $\Delta(\lambda)$ that play the role of standard modules.
- The **dual Weyl modules** $\nabla(\lambda)$ that play the role of costandard modules.
- The **simple modules** $L(\lambda)$ that play the role of atoms. These are not addressed in this notebook.
- The **indecomposable tilting modules** $T(\lambda)$ that play the role of projective modules.

As usual in representation theory, we would like to understand the characters of these modules. For the first two this is easy: $\Delta(\lambda)$ and $\nabla(\lambda)$ have the same characters as the simple (quantum) $\mathfrak{sp}_{2n}$-modules in the semisimple case which are given by (the quantum version of) Weyl's character formula. In other words, they are **known**.

Let $\varpi_{i}$ be the ith fundamental weight of the symplectic group where we use the convention that the double edge of the Dynkin diagram of $\mathfrak{sp}_{2n}$ is from $n-1$ to $n$. Then the tilting characters (we denote these using square brackets) are given as follows.

First, the initial conditions are
$[T_{\mathbb{K}}(\varpi_{0})]=[\Delta_{\mathbb{K}}(\varpi_{0})]$ (the trivial modules) and $[T_{\mathbb{K}}(\varpi_{1})]=[\Delta_{\mathbb{K}}(\varpi_{1})]$. Then, for $k>1$:
$$[T_{\mathbb{K}}(\varpi_{k})]=\sum_{i\geq 0,k-2i\geq 0}[\Delta_{\mathbb{K}}(\varpi_{k-2i})]-\sum_{i\geq 1,k-2i\geq 0,\binom{n-k}{i}\neq 0}[T_{\mathbb{K}}(\varpi_{k-2i})].$$
(Here $\binom{n-k}{i}$ is the quantum binomial.)
Note that this **determines them** as the Weyl characters are known.

The Mathematica notebook computes these characters. 

# Running the notebook

To do

# Example

For example, for $n=78$ and quantum characteristic $p=7,\ell=3$ and $p=3,\ell=2$, respectively, we get:

<div style="text-align: center"><img src="https://www.dtubbenhauer.com/papers/spweyl1.png" width="500" height="504" style="border: 0px;" /></div><div style="text-align: center"><img src="https://www.dtubbenhauer.com/papers/spweyl2.png" width="500" height="504" style="border: 0px;" /></div>

The columns are the fundamental tilting modules $T(\varpi_{i-1})$ and the rows the fundamental Weyl modules $\Delta(\varpi_{i-1})$, both starting to count at one.
