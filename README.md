## EX. NO: 1(A) : IMPLEMENTATION OF CAESAR CIPHER
 

## AIM:

To implement the simple substitution technique named Caesar cipher using C language.

## DESCRIPTION:

To encrypt a message with a Caesar cipher, each letter in the message is changed using a simple rule: shift by three. Each letter is replaced by the letter three letters ahead in the alphabet. A becomes D, B becomes E, and so on. For the last letters, we can think of the
alphabet as a circle and "wrap around". W becomes Z, X becomes A, Y bec mes B, and Z
becomes C. To change a message back, each letter is replaced by the one three before it.

## EXAMPLE:

![image](https://github.com/Hemamanigandan/CNS/assets/149653568/eb9c6c43-8c80-4cdd-b9d4-91705a311c79)


## ALGORITHM:

### STEP-1: Read the plain text from the user.
### STEP-2: Read the key value from the user.
### STEP-3: If the key is positive then encrypt the text by adding the key with each character in the plain text.
### STEP-4: Else subtract the key from the plain text.
### STEP-5: Display the cipher text obtained above.

## PROGRAM:
```
Name: Jayakumar B
Register nymber: 212223040073
```

```PY
def caesar_cipher(text, key, encrypt=True):
    result = ""
    
    for char in text:
        if char.isalpha():
            shift = key if encrypt else -key
            base = ord('A') if char.isupper() else ord('a')
            result += chr((ord(char) - base + shift) % 26 + base)
        else:
            result += char
    
    return result


# Get user input

plain_text = input("Enter the plain text: ")

key = int(input("Enter the key value: "))

# Encryption
encrypted_text = caesar_cipher(plain_text, key)

# Print plain text first, then encrypted text
print("\nPlain Text:", plain_text)
print("\nEncrypted Text:", encrypted_text)

```

## OUTPUT :

![image](https://github.com/user-attachments/assets/719b20c6-1234-4a72-b79e-f7f47a0b4086)

## RESULT :
    Thus the program for Caesar Cipher is implemented successfully.
