---
date created: Monday, September 19th 2022, 10:34:38 am
date modified: Monday, October 3rd 2022, 8:39:55 am
---

# Week 9

## Gram–Schmidt Orthonormalisation

Let V be a *finite*-dimensional inner product space. Then

1. if $S \subset V$ is orthonormal, then $S$ is linearly independent;
2. any orthonormal set $S \subset V$ can be extended to an orthonormal basis of $V$.

## Orthogonal Complement

If $V$ is a *finite*-dimensional inner product space and $W$ is a subspace, then

1. $W^\bot$ is a subspace of $V$;
2. $W \cap W^\bot = \{0\}$;
3. $V = W + W^\bot$;
4. $V = W \oplus W^\bot$;
5. $\dim W^\bot = \dim V - \dim W$.

## Adjoint Transformations

An *adjoint* of $f$ is a linear transformation $f^*: V \to V$ satisfying $(f(v), w) = (v, f^*(w))$ for all $v, w \in V$.

If $V$ is finite-dimensional, then $f^*$ exists and is unique.

Moreover, if $A$ is the matrix of $f$ with respect to an orthonormal basis $\mathcal B$, then the matrix of $f^*$ with respect to $\mathcal B$ is $A^* = \overline A^T$.

---

(Properties of adjoints) Let $f, g: V \to V$ , $a \in K$. We have

- $(f + g)^* = f^* + g^*$
- $(af)^* = \overline a f^*$
- $(f \circ g) = g^* \circ f^*$
- $(f^*)^* = f$

| property                    | generic name | over $\mathbb R$ | over $\mathbb C$ |
| --------------------------- | ------------ | ---------------- | ---------------- |
| $f^* = f$                   | self-adjoint | symmetric        | Hermitian        |
| $f^* \circ f = \text{id}_V$ | isometry     | orthogonal       | unitary          |
| $f \circ f^* = f^* \circ f$ | normal       |                  |                  |
