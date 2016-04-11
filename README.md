# node-steam-crypto

Node.js implementation of Steam crypto. All keys and data are passed as Buffers.

## verifySignature(data, signature[, algorithm])

Verifies an RSA signature using the Steam system's public key. `data` and `signature` should both be Buffers. `algorithm` defaults to "RSA-SHA1". Returns `true` if the signature is valid, or `false` if not.

## generateSessionKey()

Generates a 32 byte random blob of data and encrypts it with RSA using the Steam system's public key. Returns an object with the following properties:
* `plain` - the generated session key
* `encrypted` - the encrypted session key

## symmetricEncrypt(input, sessionKey)

Encrypts `input` using `sessionKey` and returns the result.

## symmetricDecrypt(input, sessionKey)

Decrypts `input` using `sessionKey` and returns the result.
