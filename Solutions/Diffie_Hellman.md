## Diffie Hellman
p = 991 and  g = 209. Task is to find the integer d

## Python code 
```bash
def egcd(a, b):
    if b == 0:
        return (a, 1, 0)
    g, x1, y1 = egcd(b, a % b)
    x = y1
    y = x1 - (a // b) * y1
    return (g, x, y)

p = 991
g = 209
gcd, x, y = egcd(g, p)
if gcd != 1:
    raise ValueError("Inverse does not exist")
d = x % p
print(d)
```
## Result

<img width="272" height="29" alt="image" src="https://github.com/user-attachments/assets/c5571818-e571-4842-a0c8-50d1a81e0b4d" />

## Generators of a Group 
p = 28151.Find the smallest g > 1. To verify that g is a generator, it must satisfy:g^((p-1)/q) mod p != 1 for every prime factor q of (p-1).

## Python code
```bash
p = 28151


def prime_factors(n):
    pf = set()
    d = 2
    while d * d <= n:
        while n % d == 0:
            pf.add(d)
            n //= d
        d += 1 if d == 2 else 2
    if n > 1:
        pf.add(n)
    return sorted(pf)

factors = prime_factors(p-1)  

def is_primitive_root(g):
    for q in factors:
        if pow(g, (p-1)//q, p) == 1:
            return False
    return True

for g in range(2, p):
    if is_primitive_root(g):
        print("Smallest primitive root modulo", p, "is", g)
        # verification
        print("Checks:", [(q, pow(g, (p-1)//q, p)) for q in factors])
        break
```

## Result

<img width="399" height="40" alt="image" src="https://github.com/user-attachments/assets/205b7740-e649-42c8-8bcd-558c78b60085" />
