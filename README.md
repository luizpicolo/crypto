# Encryption and Decryption using Node.js

This code provides a simple way to encrypt and decrypt text using the Advanced Encryption Standard (AES) algorithm in Cipher Block Chaining (CBC) mode with Node.js's `crypto` module.

## Pre requisites

Before using this code, make sure you have Node.js installed on your system.

## Usage

1. **Import the Module**

   First, import the `encrypt` and `decrypt` functions from the module in your Node.js project.

   ```javascript
   const crypto = require('./crypto');
   ```

2. **Set Encryption Parameters**

   Modify the following constants in your code with your own values:
   
   - `CHAVE`: A 32-character encryption key.
   - `IV`: A 16-character initialization vector.
   - `ALGORITMO`: The encryption algorithm, which is set to "aes-256-cbc" by default. You can change it if needed.
   - `METODO_CRIPTOGRAFIA` and `METODO_DESCRIPTOGRAFIA`: The methods used for encoding the output. They are set to 'hex' by default.

3. **Encrypt Text**

   To encrypt a piece of text, call the `encrypt` function and pass the text as a parameter.

   ```javascript
   const textToEncrypt = 'This is a secret message';
   const encryptedText = crypto.encrypt(textToEncrypt);
   ```

4. **Decrypt Text**

   To decrypt the encrypted text, call the `decrypt` function and pass the encrypted text as a parameter.

   ```javascript
   const decryptedText = crypto.decrypt(encryptedText);
   ```

5. **Complete Example**

   Here's a complete example of how to use the code:

   ```javascript
   const crypto = require('./crypto');

   const CHAVE = 'bf3c199c2470cb477d907b1e0917c17e';
   const IV = '5183666c72eec9e4';

   // Encrypt
   const textToEncrypt = 'This is a secret message';
   const encryptedText = crypto.encrypt(textToEncrypt);
   console.log('Encrypted:', encryptedText);

   // Decrypt
   const decryptedText = crypto.decrypt(encryptedText);
   console.log('Decrypted:', decryptedText);
   ```

## Security Note

Make sure to keep your encryption key (`CHAVE`) and initialization vector (`IV`) secret and secure, as they are critical for the security of your encrypted data.

---

Feel free to replace the placeholders with your actual values and use this README as a guide to integrate encryption and decryption into your Node.js project.