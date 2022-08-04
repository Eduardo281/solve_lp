# Solve_lp
## A CLI to solve Linear Programming Problems

### Introduction
`Solve_LP` is a CLI (Command Line Interface) developed to be an <strong>easy</strong> tool to solve Linear Programming Problems (real, integer or mixed-integer). Since it is fully implemented in Python, `Solve_LP` is Operational System independent, that is, any device having a Python interpreter installed can run it in its terminal.

<strong>IMPORTANT NOTE:</strong> In this <strong>Readme</strong> file we present its basic usage and a summary of possible arguments. For a complete usage guide, please refer to the <strong>User Guide</strong> available in this repository.

Before we begin, we should emphasize that `Solve_LP`:

<ul>
    <li> It's <strong>NOT</strong> a modeling language;</li>
    <li> It's <strong>NOT</strong> a MILP solver;</li>
</ul>

In fact, `Solve_LP` it's a tool developed to solve MILP problems by calling common powerful modeling languages/linear programming solvers through simple command line instructions.

### Basic Usage
`Solve_LP` works based on the matricial representation of a Linear Programming problem, where:

$\bullet$ $x$ represents the decision variables;

$\bullet$ $c$ represents the costs vector;

$\bullet$ $b$ represents the resources vector (a.k.a. the RHS - Right Hand Side - vector);

$\bullet$ $A$ represents the (...)

In which follows, it's considered as a linear programming problem in <i>standard format</i> a minimization problem where all the constraints are equalities and all the variables are greater than zero and do not have any upper bound, what can be denoted by:

$$
    \begin{array}{llc}
        \min & & c^T x \\
        \operatorname{s.t.} & & Ax = b \\
        & & x \geqslant 0
    \end{array}
$$

To better describe the basics about how to use `Solve_LP`, we will start by defining our first example, which is a simple real linear programming problem in standar format. Problems including other kinds of constraints, considering integer variables and setting up solving parameters will be discussed ahead.


<div style="display: flex; justify-content: space-between">
    <span>
        LEFT TEXT
    </span>
    <span>
        RIGHT TEXT
    </span>
</div>

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
        \max                & & c^T x          \\
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
    x_1, ..., x_4 \geqslant 0
    \end{array}
$$