﻿# EasyNetPGP

EasyNetPGP is an easy and straightforward PGP wrapper Library for the .NET Framework.

The BouncyCastle Cryptography Libraries are utilized for Key Pair Generation, as well as Encryption and Decryption of files. 

## Installation

This package is available on NuGet from the following link:

[EasyNetPGP](https://www.nuget.org/packages/EasyNetPGP/)

## Use the Package

* Generate Public / Private Key Pairs
``` csharp
    KeyGenerator.GenerateKeyPair("test@gmail.com", "password123", @"C:\Temp");
    or
    KeyGenerator.GenerateKeyPair("test@gmail.com", "password123", @"C:\Temp", "private.asc", "public.asc");
```

* Encrypt a File
``` csharp
    PgpEncryptorDecryptor.EncryptFile(@"C:\Temp\EncryptedText.txt", @"C:\Temp\PlainText.txt", @"C:\Temp\public.asc");
```

* Decrypt a File
``` csharp
   PgpEncryptorDecryptor.DecryptFile(@"C:\Temp\EncryptedText.txt", @"C:\Temp\public.asc", "password123", @"C:\Temp\PlainText.txt") 