#### mahmoud
## Challenge Name --> genfei
## challenge link [here](https://cybertalents.com/challenges/cryptography/genfei)

### Solution description:
*Encyption

we want to understanding the given function to solve the problems

found the main idea is The reverse operation of XOR is also XOR
** i.e x^y=z, y=x^z, x=y^z

*Decryption
#### First
we will not change anything in the imports or the function F() which do xor operation then it's the reverse of itself
 
#### second
1-
```python
        tempa = a
        d = d ^ 1337
        a = c ^ (F(d | F(d) ^ d))
        b = b ^ (F(d ^ F(a) ^ (d | a)))
        c = tempa ^ (F(d | F(b ^ F(a)) ^ F(d | b) ^ a))
```
       
        
2-
```python
      tempa = a
      a = d ^ 31337
      d = c ^ (F(a | F(a) ^ a))
      c = b ^ (F(a ^ F(d) ^ (a | d)))
      b = tempa ^ (F(a | F(c ^ F(d)) ^ F(a | c) ^ d))
```

 3- repeat these steps 32 to decrypt flag  
 
 ## Finally:
the flag appears and remove the extra `<#>` then submit.



