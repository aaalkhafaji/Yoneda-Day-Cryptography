# Yoneda-Day-Cryptography
Categorical-Crypto-DAV
# Categorical Cryptography: Yoneda-Day Presheaf Framework

This repository contains the academic proof-of-concept implementation for the paper:
**"Categorical Cryptography: A Defender–Attacker–Verifier Framework for Structural Hardness via Yoneda–Day Presheaves"**

This code bridges the gap between high-level category theory and executable software, demonstrating the $O(n)$ efficiency of Day convolution over elliptic curve support bounds and the $O(n^2)$ validation complexity of the structural transition matrix.

## The Defender-Attacker-Verifier (DAV) Model
Unlike classical ECC, which relies solely on algebraic hardness, this cryptosystem introduces a structural interdiction game:
* **Defender:** Encodes payloads into a finitely presented presheaf $\mathcal{M}$ and masks it via Day convolution $\mathcal{M} \otimes_{Day} \mathcal{Y}(V_B)$.
* **Attacker:** Attempts to malleate the ciphertext support or internal morphisms.
* **Verifier:** Enforces admissibility by checking the affine gauge of the Ext^1 transition matrix (the "brick invariant") before algebraic decryption.

## Installation & Execution
This proof-of-concept requires Python 3.8+ and `numpy`.

```bash
pip install -r requirements.txt
Run the 4608-bit bandwidth bandwidth test ($n=16$):Bashpython -m examples.run_4608_bit_test
Run the DAV structural hardness unit tests:Bashpytest tests/
Note: This repository is intended for academic peer-review and structural validation. It is not optimized for constant-time execution against side-channel attacks and should not be used in production environments.
---

