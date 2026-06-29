---
# Render all $...$ and $$...$$ with the official Typst compiler (MathML output)
mathRenderer: typst
theme: default
title: Typst Math in Slidev
info: |
  ## Typst Math Showcase
  Demonstrates the `mathRenderer: typst` feature — math written in Typst
  syntax, rendered to native MathML by the official Typst 0.15 compiler.
---

# Typst Math in Slidev

Write math in **Typst syntax** instead of LaTeX

Rendered to native **MathML** by the official Typst compiler

<div class="abs-br m-6 text-sm opacity-50">
mathRenderer: typst
</div>

---

# Inline Math

Typst math flows naturally inside text.

For a vector $bold(v) in RR^n$, the Euclidean norm is
$norm(bold(v)) = sqrt(sum_(i=1)^n v_i^2)$.

```markdown
For a vector $bold(v) in RR^n$, the Euclidean norm is
$norm(bold(v)) = sqrt(sum_(i=1)^n v_i^2)$.
```

A function $f: A -> B$ is *injective* if
$f(a_1) = f(a_2) ==> a_1 = a_2$.

```markdown
A function $f: A -> B$ is *injective* if
$f(a_1) = f(a_2) ==> a_1 = a_2$.
```

The golden ratio is $phi = (1 + sqrt(5)) / 2 approx 1.618$.

```markdown
The golden ratio is $phi = (1 + sqrt(5)) / 2 approx 1.618$.
```

<div class="mt-4 text-sm opacity-60">

Note the Typst syntax: `bold(v)`, `RR`, `norm(...)`, `sqrt(...)`, `->`, `==>`.

</div>

---

# Block Math

Euler's identity:

$$
e^(i pi) + 1 = 0
$$

The Gaussian integral:

$$
integral_(-infinity)^infinity e^(-x^2) d x = sqrt(pi)
$$

A binomial sum:

$$
sum_(k=0)^n binom(n, k) = 2^n
$$

---

# Matrices & Vectors

A linear transformation:

$$
mat(1, 2; 3, 4) vec(x, y) = vec(x + 2y, 3x + 4y)
$$

The identity matrix:

$$
I_3 = mat(
  1, 0, 0;
  0, 1, 0;
  0, 0, 1;
)
$$

---

# Piecewise Definitions

The absolute value as a piecewise function:

$$
abs(x) = cases(
  x   & "if" x >= 0,
  -x  & "if" x < 0,
)
$$

The sign function:

$$
op("sgn")(x) = cases(
  1   & "if" x > 0,
  0   & "if" x = 0,
  -1  & "if" x < 0,
)
$$

---

# Line Highlighting

Click through to reveal Maxwell's equations one line at a time:

$$ {1|2|3|4|all}
nabla dot bold(E)   &= rho / epsilon_0 \
nabla dot bold(B)   &= 0 \
nabla times bold(E) &= - (partial bold(B)) / (partial t) \
nabla times bold(B) &= mu_0 bold(J) + mu_0 epsilon_0 (partial bold(E)) / (partial t)
$$

<div class="mt-4 text-sm opacity-60">

Syntax: <code>$$ &#123;1|2|3|4|all&#125;</code> — each `\` starts a new highlightable line.

</div>

---

# Aligned Derivations

$$ {1-2|3|all}
(x + 1)^2 &= (x + 1)(x + 1) \
          &= x^2 + x + x + 1 \
          &= x^2 + 2x + 1
$$

Highlight ranges work just like KaTeX: single lines (`3`), ranges (`1-2`),
multiple (`1|3`), and `all`.

---
layout: center
---

# It just works

All math on these slides was compiled by the **official Typst 0.15 Rust
implementation** to **native MathML** — selectable, accessible, and
zero client-side JS.

$$
sum_("Typst" + "Slidev") = suit.heart
$$
