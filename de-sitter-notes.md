# de Sitter Space – Notes

## 1. What I think it is
De Sitter space is a maximally symmetric solution to Einstein's field equations with a positive cosmological constant \(\Lambda>0\). Its curvature radius is
\[
\ell = \sqrt{\frac{3}{\Lambda}}\quad(\text{in }3+1\text{ dimensions}),
\]
and its expansion in cosmological slicings is exponential at late times. Unlike Anti-de Sitter space, it does not have a timelike conformal boundary; instead, observers encounter cosmological horizons that limit causal access.

## 2. Why it matters
- **Cosmological Accuracy:** It is the closest simple geometric model of the late-time, dark-energy-dominated accelerating universe (while realistic cosmology is FLRW + matter/radiation + \(\Lambda\)).
- **Early Universe:** Quasi-de Sitter spacetime is the standard approximation used during inflationary model building.
- **The Open Problem:** A complete, nonperturbative quantum-gravity description of de Sitter space remains unsolved and is not captured by standard AdS/CFT tools.

## 3. What I don’t understand
- **Metric Tensor Transformation:** How analytic continuation (Wick rotation plus parameter continuation) maps AdS metrics to dS metrics component-by-component.
- **Boundary Mapping:** How attempts at holography in de Sitter space reinterpret “boundary data” at future infinity \(\mathcal{I}^+\) rather than at a spatial timelike wall.
- **Domain Walls:** How brane/domain-wall constructions in higher dimensions can induce effective 4D expanding cosmologies.

## 4. Questions
1. How exactly does the boundary of a de Sitter universe get mapped onto infinite future time?
2. What happens to unitarity when attempting to define a quantum theory from data at \(\mathcal{I}^+\)?
3. What are explicit coordinate transformations I can implement in a script to move between common de Sitter charts?

## 5. Concrete formulas to compute with
### 5.1 Global coordinates
\[
ds^2=-dt^2+\ell^2\cosh^2\!\left(\frac{t}{\ell}\right)d\Omega_3^2.
\]

### 5.2 Flat FLRW (Poincaré) patch
\[
ds^2=-d\tau^2+e^{2H\tau}d\mathbf{x}^2,\qquad H=\frac{1}{\ell}.
\]
Equivalent conformal-time form with \(\eta<0\):
\[
ds^2=\frac{1}{(H\eta)^2}\left(-d\eta^2+d\mathbf{x}^2\right),\qquad \eta=-\frac{e^{-H\tau}}{H}.
\]

### 5.3 Static patch
\[
ds^2=-(1-H^2r^2)dt_s^2+\frac{dr^2}{1-H^2r^2}+r^2d\Omega_2^2,
\]
with horizon at \(r=H^{-1}=\ell\).

### 5.4 Embedding-space definition (useful for checks)
De Sitter \(dS_4\) is the hyperboloid in \(\mathbb{R}^{1,4}\):
\[
-X_0^2+X_1^2+X_2^2+X_3^2+X_4^2=\ell^2.
\]
Deriving charts from this embedding is often the most robust route for symbolic scripts.
