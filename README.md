# Quantum QFT Adder

The QFT adder implements

$$
|a\rangle |b\rangle \longmapsto |a\rangle |(a + b) \bmod 2^{n}\rangle
$$

The circuit works in three steps:

1. Apply the QFT to the b‑register to encode b in phases:

$$
|a\rangle |b\rangle \longmapsto |a\rangle \mathrm{QFT}|b\rangle
$$

2. Use controlled phase rotations from the a‑register on the QFT‑encoded b‑register to add a in the phase domain:

$$
|a\rangle \mathrm{QFT}|b\rangle \longmapsto |a\rangle \mathrm{QFT}|a + b\rangle
$$

3. Apply the inverse QFT to recover the sum in the computational basis:

$$
|a\rangle \mathrm{QFT}|a + b\rangle \longmapsto |a\rangle |(a + b) \bmod 2^{n}\rangle
$$
