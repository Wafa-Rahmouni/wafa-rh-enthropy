import math

l, u, d, s, entropy = 0, 0, 0, 0, 0
range2 = (25, 50)
range3 = (50, 75)
range4 = (75, 100)
special = "~!@#$%^&*_-+=`|\(){}[]:;'<>,.?/ "
print("Please enter your password:[5-127] characters")
password = input()
# counting password length
while len(password) not in range(5, 127):
    print("Invalid Password, please try another one:")
    password = input()
for i in password:
    # counting lowercase alphabets
    if i.islower():
        l += 1
    # counting uppercase alphabets
    if i.isupper():
        u += 1
    # counting digits
    if i.isdigit():
        d += 1
    # counting special characters
    if i in special:
        s += 1
# checking strength
"""S indicates the pool size of the characters mentioned in the given password"""
S = 0
if l > 0:
    S = 26
if u > 0:
    S += 26
if d > 0:
    S += 10
if s > 0:
    S += 32
entropy = round(len(password) * math.log2(S), 1)
print("Your password has:")
print(f'{l} lowercase letters.')
print(f'{u} uppercase letters.')
print(f'{d} digits.')
print(f'{s} special characters.')
print("Your password's entropy is:", entropy, "bits")
print("Remarks:")
if entropy < 25:
    print("Poor password, better be changed")
if 25 < entropy < 50:
    print("Reasonable password, you can do better")
if 50 < entropy < 75:
    print("Strong password")
if 75 < entropy < 100:
    print("Very strong password")
if entropy > 100:
    print("Excellent password!")
