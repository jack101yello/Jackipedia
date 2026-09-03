# Plethystic Exponentiation

Plethystic exponentiation is an exponentiation operation of particular use when computing the [[Witten Index|Witten index]] of a supersymmetric theory. For a multi-variable function $f$ of variables $x_i$, we define:

$$
\text{PE}[f(x_i)] = \exp\left( \sum_{n=1}^{\infty} \frac{1}{n} f(x_i^n) \right), \quad \tilde{\text{PE}}[f(x_i)] = \exp\left( -\sum_{n=1}^{\infty} (-1)^n \frac{1}{n} f(x_i^n) \right)
$$

For instance:

$$
\text{PE}[x] = \exp\left(\sum_{n=1}^{\infty} \frac{x^n}{n}\right) = \exp \log \frac{1}{1-x} = \frac{1}{1-x}
$$

$$
\tilde{\text{PE}}[x] = \exp\left(-\sum_{n=1}^{\infty} (-1)^n \frac{x^n}{n} \right) = \exp \log(1+x) = 1+x
$$