# Solve_lp
## A CLI to solve Linear Programming Problems

### Introduction
`Solve_LP` is a CLI (Command Line Interface) developed to be an <strong>easy</strong> tool to solve Linear Programming Problems (real, integer or mixed-integer). Since it is fully implemented in Python, `Solve_LP` is Operational System independent,that is, any device having a Python interpreter installed can run it in its terminal.

<strong>IMPORTANT NOTE:</strong> In this <strong>Readme</strong> file we present its basic usage and a summary of possible arguments. For a complete usage guide, please refer to the <strong>User Guide</strong> available in this repository.

### Basic Usage
STANDARD LINEAR PROGRAMMING (...)

$$
    \begin{array}{llc}
        \min & & c^T x \\
        \operatorname{s.t.} & & Ax = b \\
        & & x \geqslant 0
    \end{array}
$$

FIRST EXAMPLE:

$$
    \begin{array}{llrcrcrcrcrcr}
    \min                & & 7x_1 & + & 9x_2 & + & 8x_3 & + & 5x_4 & + & 4x_5 &   &    \\
    \operatorname{s.t.} & & 9x_1 & + & 4x_2 & + & 6x_3 & + & 6x_4 & + & 5x_5 & = & 42 \\
                        & & 4x_1 & + & 8x_2 & + & 3x_3 & + & 4x_4 & + & 1x_5 & = & 62 \\
                        & & 8x_1 & + & 5x_2 & + & 5x_3 & + & 4x_4 & + & 7x_5 & = & 46
    \end{array}
$$ 
$$
    \begin{array}{c}
    x_1, ..., x_5 \geqslant 0
    \end{array}
$$

SOLUTION /\

$$x_1 = 0, x_2 = \frac{20}{3}, x_3 = 0, x_4 = 2, x_5 = \frac{2}{3}$$

OTHER COMMON FORMAT:
$$
    \begin{array}{llc}
        \max & & c^T x \\
        \operatorname{s.t.} & & Ax \leqslant b \\
        & & x \geqslant 0
    \end{array}
$$

SECOND EXAMPLE:

$$
    \begin{array}{llrcrcrcrcr}
    \max                & & 91x_1 & + & 85x_2 & + & 88x_3 & + & 87x_4 &  \\
    \operatorname{s.t.} & & 25x_1 & + & 25x_2 & + & 24x_3 & + & 26x_4 & \leqslant & 40 \\
                        & & 56x_1 & + & 61x_2 & + & 60x_3 & + & 59x_4 &  \leqslant & 112 \\
                        & &  5x_1 & + &  6x_2 & + &  7x_3 & + &  9x_4 &  \leqslant & 20
    \end{array}
$$ 
$$
    \begin{array}{c}
    x_1, ..., x_5 \geqslant 0
    \end{array}
$$