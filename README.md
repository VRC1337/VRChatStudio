# VRChat Studio

This project is specifically designed for decrypting VRChat cache files, forked from [Escartem/AnimeStudio](https://github.com/Escartem/AnimeStudio).

## How to Use

1. Calculate a 256-bit AES key and encode it in hexadecimal format

2. Rename the file you wish to decrypt to this encoded result

3. Use this tool to load the file for decryption and extraction

Example:

`__data` → `8eff42f4db976b62c027fce0f251ecb5e25b18f98ab3ecef55e27b563eb9d92a`

## For VRCW Files

Use the `id` to calculate the key:

```
SHA256.HashData(Encoding.UTF8.GetBytes("wrld_7e10376a-29b6-43af-ac5d-6eb72732e90c" + "-MKEf6MXxgp5zN4YZkSdoj3oVygj6rLDTLXk6BQHnpyCRdv6R7d8Hm4nGs6LwQ9Ce"));
```

## VRCA

Use the `encryptionKey` to calculate the key:

```
Convert.FromBase64String("jv9C9NuXa2LAJ/zg8lHsteJbGPmKs+zvVeJ7Vj652So=")
```

| ⚠️ This tool does not provide methods for extracting the `encryptionKey`.

---

Special thanks to:
- Perfare: [AssetStudio](https://github.com/perfare/AssetStudio)
- Escartem: [AnimeStudio](https://github.com/Escartem/AnimeStudio)
