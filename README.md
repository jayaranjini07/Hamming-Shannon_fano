# Huffman-Shannon_fano
# Aim:
Consider a discrete memoryless source with symbols and statistics {0.125, 0.0625, 0.25, 0.0625, 0.125, 0.125, 0.25} for its output. 
Apply the Huffman and Shannon-Fano to this source. 
Show that by drawing the tree diagram, and 
Calculate the average code word length, entropy, variance, redundancy, and efficiency.
# Tools Required:
Google colab
# Program:
```
import math

p = [0.55,0.15,0.15,0.1,0.005]
lk = [3, 4, 2, 4, 3, 3, 2]
n = len(p)

# Average Codeword Length
L = sum(p[k] * lk[k] for k in range(n))

# Entropy
hs = sum(p[k] * math.log(1 / p[k], 2) for k in range(n))
hs = round(hs, 3)

# Efficiency
eff = round(hs / L, 3)

# Redundancy
red = round(1 - eff, 3)

# Variance
var = sum(p[k] * (lk[k] - L) ** 2 for k in range(n))
var = round(var, 3)

# Output
print(f"Average Codeword Length is : {L}")
print(f"Entropy is : {hs}")
print(f"Efficiency is : {eff * 100}%")
print(f"Redundancy is : {red}")
print(f"Variance is : {var}")
```
![WhatsApp Image 2025-09-20 at 15 34 41_f46832e9](https://github.com/user-attachments/assets/cce9d728-ca7c-47a2-9dae-cecdab4569ca)

# Output
<img width="466" height="131" alt="image" src="https://github.com/user-attachments/assets/656d3887-4eec-4b79-ba19-6f3c3d204859" />

# Results:
The experiment was successfully executed.
