# 2025-Quantum-Factorization-With-Quantum-Rings

This project demonstrates the implementation of Shor's algorithm using Quantum Rings. Shor's algorithm is a quantum algorithm for integer factorization, which runs exponentially faster than the best-known classical algorithms.

## Setup and Installation

1. **Clone the repository:**
    ```bash
    git clone https://github.com/your-repo/2025-Quantum-Factorization-With-Quantum-Rings.git
    cd 2025-Quantum-Factorization-With-Quantum-Rings
    ```

2. **Create a virtual environment:**
    ```bash
    conda create -n quantum-rings python=3.11
    conda activate quantum-rings
    ```

3. **Install the required packages:**
    ```bash
    pip install -r requirements.txt
    ```

## Running the Project

1. **Open Jupyter Notebook:**
    ```bash
    jupyter notebook
    ```

2. **Run the `Shor15.ipynb` notebook:**
    - Navigate to the `Shor15.ipynb` file in the Jupyter Notebook interface.
    - Open the notebook and run all cells to see the implementation and results of Shor's algorithm.

## Understanding Shor's Algorithm

Shor's algorithm is designed to factorize large integers efficiently using quantum computing. The algorithm consists of two main parts:

1. **Classical Part:**
    - Choose a random integer `a` such that `1 < a < N` (where `N` is the number to be factorized).
    - Compute the greatest common divisor (GCD) of `a` and `N`. If the GCD is not 1, then `a` is a factor of `N`.

2. **Quantum Part:**
    - Use quantum parallelism to find the period `r` of the function `f(x) = a^x mod N`.
    - Once the period `r` is found, use it to compute the factors of `N`.

### Example

Let's factorize `N = 15` using Shor's algorithm:

1. **Choose `a = 7`.**
2. **Compute GCD(7, 15) = 1.**
3. **Quantum Part:**
    - Find the period `r` of `f(x) = 7^x mod 15`. The period `r` is 4.
4. **Compute factors:**
    - `gcd(7^(4/2) - 1, 15) = gcd(48, 15) = 3`
    - `gcd(7^(4/2) + 1, 15) = gcd(50, 15) = 5`

Thus, the factors of 15 are 3 and 5.

## References

- [Shor's Algorithm - Wikipedia](https://en.wikipedia.org/wiki/Shor%27s_algorithm)
- [Shor's Algorithm — Quantum Rings SDK](https://portal.quantumrings.com/doc/Shors.html)
- [Shor/Qiskit/qiskit-shor-15-steps.ipynb](https://github.com/usamisaori/Shor/blob/master/Qiskit/qiskit-shor-15-steps.ipynb)
- [qiskit-community-tutorials/algorithms/shor_algorithm.ipynb](https://github.com/qiskit-community/qiskit-community-tutorials/blob/master/algorithms/shor_algorithm.ipynb)
