START
Basic
Front: Define and prove the interpolation theorem
Back: 
For any integer $n≥0$ and any list of $n+1$ points $(x_1,y_1),(x_2,y_2),...,(x_{n+1},y_{n+1})$ in $\mathbb{R}^2$ with $x1 < x2 < ··· < x_{n+1}$, there exists a unique polynomial $p(x)$ of degree at most $n$ such that $p(x_i)=y_i$ for all $i$.

**Existence**: construct the polynomial as follows: $f(x)=\sum\limits_{i=1}^n{y_i}\cdot\left(\prod\limits_{j\ne i}\frac{x-x_j}{x_i-x_j}\right)$
Clearly the constructed polynomial has a degree at most $n$ because each term has a degree of at most $n$. For each $i$, plugging in $x_i$ causes all but the $i$-th term in the sum to vanish, and the $i$-th term evaluates to $y_i$, as desired.

**Uniqueness**: suppose there are two such polynomials $f(x)$ and $g(x)$. Construct a polynomial $(f-g)(x)=f(x)-g(x)$. This is a polynomial of a degree $d$: $d\le n$. Now apply the theorem from [[connection between the polynomial degree and the number of its roots]]: $f-g$ can't have more than $n$ roots, unless it's a zero polynomial. But there are $n+1$ points where $f-g$ is zero, so it has to be a zero polynomial. Consequently, which means that $f$ and $g$ are the same. QED
<!--ID: 1745138784656-->
END
