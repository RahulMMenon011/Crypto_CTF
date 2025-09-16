## ASCII code 
[67, 84, 70, 123, 65, 83, 67, 73, 73, 95, 112, 114, 49, 110, 116, 52, 98, 108, 51, 125]
## Python code 

```bash
codes = [67, 84, 70, 123, 65, 83, 67, 73, 73, 95, 112, 114, 49, 110, 116, 52, 98, 108, 51, 125]

flag = "".join(chr(c) for c in codes)
print("Flag:", flag)
```
## Result
<img width="245" height="41" alt="image" src="https://github.com/user-attachments/assets/fa3a4838-3f7b-49a3-9f18-c3cddc1c77c7" />

## HEX value 
[4354467b596f755f77696c6c5f62655f776f726b696e675f776974685f6865785f737472696e67735f615f6c6f747d]

```bash
hex_values = ["4354467b596f755f77696c6c5f62655f776f726b696e675f776974685f6865785f737472696e67735f615f6c6f747d"]

for hv in hex_values:
    flag = bytes.fromhex(hv).decode()
    print("Flag:", flag)
```
## Result
<img width="419" height="26" alt="image" src="https://github.com/user-attachments/assets/9d93c0c6-11fb-4585-94fe-a5aff36ce4b7" />
