---
Title: Diffie-Hellman Exchange
Template: LeafPage
---

**Diffie-Hellman Exchange**

The Diffie-Hellman key exchange protocol functions thus: given some $g$ (mod $p$) which Alice wishes to communicate to Bob, both Alice and Bob secretly pick some $a, b$ (mod $p$). Alice communicates $g^a$ (mod $p$) to Bob (who can then calculate $g^{ab}$ (mod $p$)). Bob then sends $g^b$ (mod $p$) to Alice. Both, then, know $s = g^{ab}$ (mod $p$) without it ever being communicated directly. As such, the determination of this key requires the evaluation of a discrete logarithm by anyone who seeks to decrypt their communications from then on; for a sufficiently large prime $p$, it is theoretically impossible to calculate in a reasonable amount of time. Much of the potential insecurity of Diffie-Hellman, however, rests on the underestimation of this word 'large'. 
