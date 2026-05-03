# Cryptography Operations Cheat Sheet

Tools and techniques for breaking common ciphers.

## Encoding/Decoding
- **Base64**: `echo "string" | base64`, `echo "hash" | base64 -d`.
- **URL Encoding**: Use CyberChef.
- **Hex**: `xxd -r -p` to convert hex to binary.

## Ciphers
- **Caesar/Rot13**: Use CyberChef or `tr 'A-Za-z' 'N-ZA-Mn-za-m'`.
- **Vigenere**: Use `vigenere-solver` or online tools.

## RSA
- **Extracting Public Key Info**: `openssl rsa -pubin -in public.pem -text -noout`.
- **RsaCtfTool**: `python3 RsaCtfTool.py --publickey public.pem --uncipherfile cipher.bin`.

## Hash Cracking
- **Hashcat**: `hashcat -m <mode> <hash_file> <wordlist>`.
- **John the Ripper**: `john --wordlist=<wordlist> <hash_file>`.
