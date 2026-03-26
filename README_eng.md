DESCRIPTION
DualSimple is a simplified implementation of automatic differentiation (AD) using dual numbers. It supports first‑order derivatives and gradients for functions of one or several real variables. This is a lightweight version suitable for problems that do not require higher‑order or fractional derivatives.

FEATURES
Dual class (dual number) with arithmetic operations.
Elementary functions (power, exponential, logarithmic, trigonometric, inverse trigonometric, hyperbolic).
Differentiation operator D(f, x) for single‑variable functions.
Differentiation operator D(f, X, index) for multivariable functions (partial derivative).
Gradient function grad(f, X).
Machine precision, linear complexity.

INSTALLATION AND BUILD
The library consists of dual_simple.h and dual_simple.cpp. To use:
Copy the DualSimple folder into your project.
Add dual_simple.cpp to your build.
Include the header:

#include "DualSimple/dual_simple.h"

Use the namespace dual_simple.
For a static library, compile dual_simple.cpp into DualSimple.lib and link it.

DEPENDENCIES
RealUtils (for convenient function names).

EXAMPLE

#include <iostream>
#include "DualSimple/dual_simple.h"
#include "RealUtils/real_utils.h"

auto f = [](dual_simple::Dual x) {
    return sin(x) * exp(x);
};

int main() {
    double x = 1.0;
    double df = dual_simple::D(f, x);
    std::cout << "f'(1) = " << df << std::endl;
    return 0;
}

License
MIT License. See the LICENSE file.

Author
Mikhail D. Sychev
Email: murzilkabest@icloud.com
Telegram: @Murz1k22

