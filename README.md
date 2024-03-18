# [[2^j ,2^j - j - 2, 3]] Gottesman's Code

This is homegrown implementation of the family of **[[2^j, 2^j - j - 2, 3]] Gottesman codes**, also known as **[[2^j, 2^j - j - 2, 3]]** **quantum Hamming codes**, as described in Gottesman's 1997 PhD thesis on '_Stabilizer Codes and Quantum Error Correction_' [1].

Key details for the [[8, 3, 3]] code when j = 3 using Stabilizer Formalism:
- [] utilizes an explicit construction method for the stabilizer generators. The remaining m generators, apart from Mx and Mz, are constructed using the check matrix [Hm|AmHm], where Hm = [c0, c1, ..., c^2m − 1]. Each column ck (for k = 0, 1, ..., 2^m − 1) represents a binary vector corresponding to the integer k. Also, Am refers to any invertible m × m matrix devoid of fixed points such that Am​.s ≠ 0 and Am.s ≠ s for all s ∈ F₂ᵐ.
- [] introduces alternative stabilizer generators for the [[8, 3, 3]] code. It identifies permutations effective for all stabilizer generators except for X^⊗8 and Z^⊗8. However, these can be replaced with XXYZIYZI and ZZIXYIXY, respectively. The stabilizer generators are permuted to achieve desired properties, reflecting an alternative approach to constructing the stabilizer code.

Notes:
- This implementation adopts the Gottesman Notation for the [[8, 3, 3]] stabilizer code as depicted in Table 3.3 on Page 22 on the Gottesman's PhD thesis. Additionally, for j = 4, our [[16, 10, 3]] stabilizer code stemming from Gottesman(4) can be cross-verified from **Table 8.1 on Page 91 **as well []
- The differences between [], [], and [] primarily lie in the choice of stabilizer generators and their permutations for the [[8, 3, 3]] stabilizer code.
"""

# Requirements

- QuantumClifford.jl

# References
- Gottesman, D. (1997). Stabilizer Codes and Quantum Error Correction [quant-ph/9705052]. arXiv:quant-ph/9705052
- 
