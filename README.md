# lz78-source-coding

This project implements **Lempel–Ziv (LZ78)** lossless compression in Python and evaluates its performance on **random symbol sequences** generated with **non-uniform probabilities**.

Symbols: {a, b, c, d}  
Probabilities: P(a)=0.5, P(b)=0.25, P(c)=0.2, P(d)=0.05

## What this project does
- Computes **source entropy** for the given symbol probabilities.
- Generates random sequences with different lengths (e.g., 20 → 5000 symbols).
- Encodes sequences using **LZ78** (dictionary-based parsing).
- Calculates:
  - Total encoded bits (**NB**)
  - **Bits per symbol** (NB / N)
  - **Compression ratio vs ASCII (8-bit)**: NB / (8N)

## Key result (summary)
As sequence length increases, compression improves (lower bits/symbol and better compression ratio).

Example results:

| N (symbols) | NB (bits) | Compression ratio NB/(8N) | Bits per symbol (NB/N) |
|-----------:|----------:|---------------------------:|------------------------:|
| 20         | 120       | 75.00%                     | 6.0000                  |
| 50         | 286       | 71.50%                     | 5.7200                  |
| 100        | 518       | 64.75%                     | 5.1800                  |
| 200        | 854       | 53.37%                     | 4.2700                  |
| 400        | 1620      | 50.62%                     | 4.0500                  |
| 800        | 3056      | 47.75%                     | 3.8200                  |
| 1000       | 3728      | 46.60%                     | 3.7280                  |
| 5000       | 16416     | 41.04%                     | 3.2832                  |

## Project structure (suggested)
