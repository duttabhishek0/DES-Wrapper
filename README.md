# DES-Wrapper
A monolithic wrapper File System Protection in a distributed storage-area network(SAN)

## Method Used: 
DES(Data Encryption Standard)

## Structure of the solution:
The solution can be divided into two parts:
1. Encryption Key Generation
2. Encryption

### Encryption Key Generation:
1. Conversion of the input key into 10 bits, thereafter further dividing it into 5-5 bits.
```cpp
void key_generator(int num, int subkey1[], int subkey2[])
```

2. Left shifting the bits one by one and then merging will give the key
```cpp
void LS1(int p10[], int left_LS1[], int right_LS1[])
```

### Encryption
The encryption is a two step process. First the alphabet or the integer number will be converted into an 8-bit binary number, further dividing it into two parts.Then the LSB 4-bits are converted into 8-bit binary.
