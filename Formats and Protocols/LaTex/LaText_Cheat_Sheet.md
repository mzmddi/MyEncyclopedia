
# LaTex Cheat Sheet

OCT 1st 2026

- [LaTex Cheat Sheet](#latex-cheat-sheet)
  - [FRACTIONS](#fractions)
  - [SQUARE ROOT SQRT](#square-root-sqrt)
  - [SUPERSCRIPT UNDERSCRIPT EXPONENTS](#superscript-underscript-exponents)
  - [SPECIAL CHARACTERS](#special-characters)
  - [GREEK CAPITAL LETTERS](#greek-capital-letters)
  - [GREEK LOWERCASE LETTERS](#greek-lowercase-letters)
  - [RELATIONAL SYMBOLS](#relational-symbols)
  - [CUMULATIVE OPERATORS](#cumulative-operators)
  - [BRACKETS AND DELIMITERS](#brackets-and-delimiters)
  - [FUNCTIONS AND OPERATORS](#functions-and-operators)
  - [ACCENTS AND DIACRITICS](#accents-and-diacritics)
  - [MATRICES AND CASES](#matrices-and-cases)
    - [Bracketed Matrix (`bmatrix`)](#bracketed-matrix-bmatrix)
    - [Parenthesized Matrix (`pmatrix`)](#parenthesized-matrix-pmatrix)
    - [Piecewise / Conditional Functions (`cases`)](#piecewise--conditional-functions-cases)
  - [TEXT AND SPACING IN MATH MODE](#text-and-spacing-in-math-mode)


## FRACTIONS

`$\frac{}{}$`

EXAMPLE => $\frac{1}{2}$

EXAMPLE => $\frac{x}{y}$

EXAMPLE => $\frac{x+y}{1 + \frac{m}{n}}$

=> first {} is num , second {} is denum

## SQUARE ROOT SQRT

`$\sqrt{}$`

EXAMPLE => $\sqrt{1}$

EXAMPLE => $\sqrt{x}$

EXAMPLE => $\sqrt{1 + x}$

EXAMPLE => $\sqrt{m + \frac{1}{x} + n + 1}$

=> anything in the {} is under the square root

## SUPERSCRIPT UNDERSCRIPT EXPONENTS

`$x_{}$`

`$x^{}$`

EXAMPLE => $x^2 + x_2 + x_x + x^x$

EXAMPLE => $x_1^2 + x^2_1$

EXAMPLE => $x_p^q + x^p_q$

EXAMPLE => $x^{\frac{1}{2}} + x_{\frac{1}{2}}$

EXAMPLE => $x^{\frac{\sqrt{1+x}}{2}} + x_{\frac{\sqrt{1+x}}{2}}$

=> If there's one value, you can omit the {} and just write it directly. (like x^2)

=> anything in the bracket becomes superscript or underscript

## SPECIAL CHARACTERS


| | | | | 
| ------------ | -------- | ---------- | ----- |
|`$\imath$` <br> $\imath$ | `$\jmath$` <br> $\jmath$ | `$\partial$` <br> $\partial$ | `$infty$` <br> $\infty$ |
|`$\wedge$` <br> $\wedge$ |`$\vee$` <br> $\vee$ | `$\neg$`  <br> $\neg$  | `$\bot$`  <br> $\bot$| 
|`$\not$` <br> $\not$ | `$\top$` <br> $\top$| `$\nabla$`  <br> $\nabla$|`$\forall$`  <br> $\forall$ | 
| | | | |


## GREEK CAPITAL LETTERS


| | | | | 
| ---- | ---- | --- | --- |
| `$\Gamma$` <br> $\Gamma$ | `$\Delta$` <br> $\Delta$ | `$\Lambda$` <br> $\Lambda$ | `$\Phi$` <br> $\Phi$ |
| `$\Pi$` <br> $\Pi$ | `$\Psi$` <br> $\Psi$ | `$\Sigma$` <br> $\Sigma$ | `$\Theta$` <br> $\Theta$ |
| `$\Upsilon$` <br> $\Upsilon$ | `$\Xi$` <br> $\Xi$ | `$\Omega$` <br> $\Omega$ | |
| | | | |

## GREEK LOWERCASE LETTERS

| | | | |
| ---- | ---- | --- | --- |
| `$\alpha$` <br> $\alpha$ | `$\nu$` <br> $\nu$ | `$\beta$` <br> $\beta$ | `$\kappa$` <br> $\kappa$ |
| `$\gamma$` <br> $\gamma$ | `$\lambda$` <br> $\lambda$ | `$\delta$` <br> $\delta$ | `$\mu$` <br> $\mu$ |
| `$\epsilon$` <br> $\epsilon$ | `$\zeta$` <br> $\zeta$ | `$\eta$` <br> $\eta$ | `$\theta$` <br> $\theta$ |
| `$\iota$` <br> $\iota$ | `$\xi$` <br> $\xi$ | `$\pi$` <br> $\pi$ | `$\rho$` <br> $\rho$ |
| `$\sigma$` <br> $\sigma$ | `$\tau$` <br> $\tau$ | `$\upsilon$` <br> $\upsilon$ | `$\phi$` <br> $\phi$ |
| `$\chi$` <br> $\chi$ | `$\psi$` <br> $\psi$ | `$\omega$` <br> $\omega$ | |
| | | | |

## RELATIONAL SYMBOLS

| | | | |
| ---- | ---- | --- | --- |
| `$\hookrightarrow$` <br> $\hookrightarrow$ | `$\Rightarrow$` <br> $\Rightarrow$ | `$\rightarrow$` <br> $\rightarrow$ | `$\Leftrightarrow$` <br> $\Leftrightarrow$ |
| `$\nrightarrow$` <br> $\nrightarrow$ | `$\mapsto$` <br> $\mapsto$ | `$\geq$` <br> $\geq$ | `$\leq$` <br> $\leq$ |
| `$\equiv$` <br> $\equiv$ | `$\sim$` <br> $\sim$ | `$\gg$` <br> $\gg$ | `$\ll$` <br> $\ll$ |
| `$\subset$` <br> $\subset$ | `$\subseteq$` <br> $\subseteq$ | `$\in$` <br> $\in$ | `$\notin$` <br> $\notin$ |
| `$\mid$` <br> $\mid$ | `$\propto$` <br> $\propto$ | `$\perp$` <br> $\perp$ | `$\parallel$` <br> $\parallel$ |
| `$\vartriangle$` <br> $\vartriangle$ | | | | 
| | | | |

## CUMULATIVE OPERATORS

| | | | |
| ---- | ---- | --- | --- |
| `$\int$` <br> $\int$ | `$\iint$` <br> $\iint$ | `$\iiint$` <br> $\iiint$ | `$\int\dots\int` <br> $\int\dots\int$ |
| `$\prod$` <br> $\prod$ | `$\sum$` <br> $\sum$ | `$\bigcup$` <br> $\bigcup$ | `$\bigcap$` <br> $\bigcap$ |
| `$\int\cdots\int` <br> $\int\cdots\int$ | | | |
| | | | |

## BRACKETS AND DELIMITERS

| | | | |
| ---- | ---- | --- | --- |
| `\left( \frac{a}{b} \right)` <br> $\left( \frac{a}{b} \right)$ | `\left[ \frac{a}{b} \right]` <br> $\left[ \frac{a}{b} \right]$ | `\left\{ \frac{a}{b} \right\}` <br> $\left\{ \frac{a}{b} \right\}$ | `\langle x \rangle` <br> $\langle x \rangle$ |
| `\left\vert x \right\vert` <br> $\left\vert x \right\vert$ | `\left\| x \right\|` <br> $\left\Vert{} x \right\Vert{}$ | `\left. \frac{df}{dx} \right\vert_{x=0}` <br> $\left. \frac{df}{dx} \right\vert_{x=0}$ | |

=> `\left` and `\right` scale the delimiters automatically to match the size of what's inside.
=> `{` and `}` require backslashes (`\{` and `\}`) because bare curly braces are reserved for LaTeX grouping.


## FUNCTIONS AND OPERATORS

| | | | |
| ---- | ---- | --- | --- |
| `\sin x` <br> $\sin x$ | `\cos x` <br> $\cos x$ | `\tan x` <br> $\tan x$ | `\lim_{x \to 0}` <br> $\lim_{x \to 0}$ |
| `\ln x` <br> $\ln x$ | `\log_{10} x` <br> $\log_{10} x$ | `\max(a, b)` <br> $\max(a, b)$ | `\min(a, b)` <br> $\min(a, b)$ |

=> Standard named functions use backslashes so they render in upright Roman font instead of math italics.


## ACCENTS AND DIACRITICS

| | | | |
| ---- | ---- | --- | --- |
| `\vec{x}` <br> $\vec{x}$ | `\hat{x}` <br> $\hat{x}$ | `\bar{x}` <br> $\bar{x}$ | `\tilde{x}` <br> $\tilde{x}$ |
| `\dot{x}` <br> $\dot{x}$ | `\ddot{x}` <br> $\ddot{x}$ | `\mathbf{v}` <br> $\mathbf{v}$ | `\mathbb{R}` <br> $\mathbb{R}$ |


## MATRICES AND CASES

### Bracketed Matrix (`bmatrix`)
`$$\begin{bmatrix} a & b \\ c & d \end{bmatrix}$$`

EXAMPLE =>
$$\begin{bmatrix} a & b \\ c & d \end{bmatrix}$$

### Parenthesized Matrix (`pmatrix`)
`$$\begin{pmatrix} 1 & 0 \\ 0 & 1 \end{pmatrix}$$`

EXAMPLE =>
$$\begin{pmatrix} 1 & 0 \\ 0 & 1 \end{pmatrix}$$

### Piecewise / Conditional Functions (`cases`)
`$$f(x) = \begin{cases} x^2 & \text{if } x \ge 0 \\ -x & \text{if } x < 0 \end{cases}$$`

EXAMPLE =>
$$f(x) =  \begin{cases}  x^2 & \text{if } x \ge 0 \\ -x & \text{if } x < 0  \end{cases}$$

=> Use `&` to align columns/conditions and `\\` to start a new line.


## TEXT AND SPACING IN MATH MODE

| | | | |
| ---- | ---- | --- | --- |
| `\text{ word }` <br> $a = b \text{ if } c > 0$ | `\,` (thin space) <br> $a\,b$ | `\quad` (1 em space) <br> $a \quad b$ | `\qquad` (2 em space) <br> $a \qquad b$ |

=> Normal spaces inside `$...$` are ignored by LaTeX, so use `\text{}` for text and `\,`, `\quad`, or `\qquad` for spacing.