## Cipher text - `svaq gur synt: PGS{whfg_n_fvzcyr_fuvsg}`

## Python code

```bash
def caesar_decrypt(ciphertext, shift):
    result = ""
    for char in ciphertext:
        if char.isalpha():
            base = ord('A') if char.isupper() else ord('a')
            result += chr((ord(char) - base - shift) % 26 + base)
        else:
            result += char
    return result

ciphertext = "svaq gur synt: PGS{whfg_n_fvzcyr_fuvsg}"

for shift in range(26):
    print(f"Shift {shift}: {caesar_decrypt(ciphertext, shift)}")
````
bruteforcing all 26 possible shifts and printing them

## Result

<img width="507" height="454" alt="image" src="https://github.com/user-attachments/assets/cc927fe7-b18f-4633-bdc5-023579d6a81d" />
