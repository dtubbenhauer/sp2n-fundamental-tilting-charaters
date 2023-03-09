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

# Running the notebook

To do

# Example

For example, for $n=78$ and quantum characteristic $p=7,\ell=3$ and $p=3,\ell=2$, respectively, we get:

<div style="text-align: center"><img src="https://www.dtubbenhauer.com/papers/spweyl1.png" width="500" height="504" style="border: 0px;" /></div><div style="text-align: center"><img src="https://www.dtubbenhauer.com/papers/spweyl2.png" width="500" height="504" style="border: 0px;" /></div>

The columns are the fundamental tilting modules $T(\varpi_{i-1})$ and the rows the fundamental Weyl modules $\Delta(\varpi_{i-1})$, both starting to count at one.
