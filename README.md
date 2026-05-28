# Encrypted Proprietary Works Archive (2025)
Encrypted valuable original works via SM4/SM3/SM2:
1. Exclusive deep analysis of Alan Turing’s Enigma-cracking Bombe machine, including H-M factor calculation methods
2. Alternative proof for the 1979 paper *On the Cycle Structure of Some Nonlinear Feedback Shift Registers*

Timestamped priority record for original GM/T-encrypted works. No plaintext files, private keys, or source code are hosted here.

## Files
All artifacts follow the same SM4-CBC + SM2 key wrap + SM3 integrity chain:
| Filename | Purpose |
|----------|---------|
| `A Note on "On the cycle structure of some nonlinear feedback shift registers".pdf` | SM4-encrypted PDF ciphertext |
| `A Note on "On the cycle structure of some nonlinear feedback shift registers".pdf.hash` | SM3 digest of the original unencrypted source |
| `A Note on "On the cycle structure of some nonlinear feedback shift registers".pdf.key` | SM4 session key wrapped with SM2 public key |
| `Enigma.pdf` | SM4-encrypted PDF ciphertext |
| `Enigma.pdf.hash` | SM3 digest of the original unencrypted source |
| `Enigma.pdf.key` | SM4 session key wrapped with SM2 public key |

## How Protection Works
1. A random 128-bit SM4 key encrypts the source PDF to the `.pdf` ciphertext file
2. The SM4 key is encrypted with SM2 using the public key below (only the holder of the matching offline private key can unwrap it)
3. The SM3 hash of the original source is saved separately for tamper verification only

## SM2 Public Key (used for all key wrapping)
04d27f6cb313fd7af638beb36e5f26c3bd78f9b5668b235859beaeb91968c01e760c301cb328f655f7db79c1f9e65faaa69015132df83e7405da0e34fb1704af63
