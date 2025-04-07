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

# Name: Muthulakshmi D
reg : 212223040122

## PROGRAM :-
```
def encrypt(text, key):
    cipher = ""
    for char in text:
        if char.isupper():
            cipher += chr((ord(char) - ord('A') + key) % 26 + ord('A'))
        elif char.islower():
            cipher += chr((ord(char) - ord('a') + key) % 26 + ord('a'))
        else:
            cipher += char
    return cipher

def decrypt(cipher, key):
    plain = ""
    for char in cipher:
        if char.isupper():
            plain += chr((ord(char) - ord('A') - key) % 26 + ord('A'))
        elif char.islower():
            plain += chr((ord(char) - ord('a') - key) % 26 + ord('a'))
        else:
            plain += char
    return plain

# Taking input
plain_text = input("Enter the plain text: ")
key = int(input("Enter the key value: "))

# Encryption
cipher_text = encrypt(plain_text, key)
print("\nPLAIN TEXT:", plain_text)
print("\nENCRYPTED TEXT:", cipher_text)

# Decryption
decrypted_text = decrypt(cipher_text, key)
print("\nAFTER DECRYPTION:", decrypted_text)
```



## OUTPUT :-
![424300351-ac014035-f555-41ff-a376-c4242a18c148](https://github.com/user-attachments/assets/9be8a407-308b-4019-b2e6-fc2be42d559e)


## RESULT:
The program is executed successfully
