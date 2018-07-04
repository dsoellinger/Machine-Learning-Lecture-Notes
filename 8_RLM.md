## Regularized loss minimization

In RLM we minimize the sum of the empirical risk and a regularization function. Intuitively, the regularization function measures the complexity of hypotheses. Another view of regularization is as a stabilizer of the learning algorithm. An algorithm is considered stable if a slight change of its input does not change its output much. 

### Definitions

> **Convex set**
> 
> A set C in a vector space (e.g., $\mathbb{R}^n$) is convex if for any two vectors $u, v \in C$, the line segment between u and v is contained in C, i.e., 
> 
> $\forall \alpha \in [0,1]: \alpha u + (1 - \alpha)v$


### RLM learning rule

Regularized Loss Minimization (RLM) is a learning rule in which we jointly minimize the empirical risk and a regularization function.

Given a regularization function $R: \mathbb{R}^d \rightarrow \mathbb{R}$, a RLM algoirthm returns a hypothesis in:

$\text{argmin}_w (L_S(w) + R(w)) \hspace{1cm} w \in \mathbb{R}^d$

**Remark:** From now on, we only consider hypothesis classes that are subsets of $\mathbb{R}^d$. Every hypothesis is a real-valued vector.

#### Popular regularization functions

**Tikhonov regularization**

$R(w) = \lambda ||w||^2$ with $\lambda > 0$

The RLM rule becomes: $A(S) \in \text{arg min}_w(L_S(w) + \lambda ||w||^2)$

**Ridge regression**

Linear regression (L2-loss) + Tikhonov regularization

$A(S) \in \text{arg min}_w(\frac{1}{m} \sum_{i=1}^m \frac{1}{2}(<w,x_i>-y_i)^2) + \lambda ||w||^2)$


