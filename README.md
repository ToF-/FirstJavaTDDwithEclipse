### Account Checksum
We need a function that can validate an account number. An account number is a nine digits string. It is said to be valid if its checksum is a multiple of 11. The checksum is calculated as follows:

    (c1*9 + c2*8 + c3*7 + c4*6 + c5*5 + c6*4 + c7*3 + c8 * 2 + c9)

Here are examples of valid account numbers:

    000000000 // 0 modulo 11 = 0
    130000000 // 1 * 9 + 3 * 8 = 33, 33 modulo 11 = 0
    000000051 // 5 * 2 + 1 * 1 = 11, 11 module 11 = 0
    123456789
    490867715
    999999990

Write a function that given an account number returns true if this account is valid, false otherwise.
