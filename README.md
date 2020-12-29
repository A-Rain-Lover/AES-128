# AES-128
AES-128 encryption algorithm implementated in C

> I did this to understand how AES works, this is not for general use since I did not focus on performance, security, etc, and I did not test it that much. So if you are looking for an AES encryption library to use in production, this is not the right one to choose. Thank you.

## Test output
I tested with an example from the original [FIPS 197](https://csrc.nist.gov/publications/detail/fips/197/final) publication
```
*** AES encrypt ***
      input :  0x00 0x11 0x22 0x33 0x44 0x55 0x66 0x77 0x88 0x99 0xAA 0xBB 0xCC 0xDD 0xEE 0xFF 
        add :  0x00 0x10 0x20 0x30 0x40 0x50 0x60 0x70 0x80 0x90 0xA0 0xB0 0xC0 0xD0 0xE0 0xF0 
       subs :  0x63 0xCA 0xB7 0x04 0x09 0x53 0xD0 0x51 0xCD 0x60 0xE0 0xE7 0xBA 0x70 0xE1 0x8C 
      shift :  0x63 0x53 0xE0 0x8C 0x09 0x60 0xE1 0x04 0xCD 0x70 0xB7 0x51 0xBA 0xCA 0xD0 0xE7 
        mix :  0x5F 0x72 0x64 0x15 0x57 0xF5 0xBC 0x92 0xF7 0xBE 0x3B 0x29 0x1D 0xB9 0xF9 0x1A 
        add :  0x89 0xD8 0x10 0xE8 0x85 0x5A 0xCE 0x68 0x2D 0x18 0x43 0xD8 0xCB 0x12 0x8F 0xE4 
       subs :  0xA7 0x61 0xCA 0x9B 0x97 0xBE 0x8B 0x45 0xD8 0xAD 0x1A 0x61 0x1F 0xC9 0x73 0x69 
      shift :  0xA7 0xBE 0x1A 0x69 0x97 0xAD 0x73 0x9B 0xD8 0xC9 0xCA 0x45 0x1F 0x61 0x8B 0x61 
        mix :  0xFF 0x87 0x96 0x84 0x31 0xD8 0x6A 0x51 0x64 0x51 0x51 0xFA 0x77 0x3A 0xD0 0x09 
        add :  0x49 0x15 0x59 0x8F 0x55 0xE5 0xD7 0xA0 0xDA 0xCA 0x94 0xFA 0x1F 0x0A 0x63 0xF7 
       subs :  0x3B 0x59 0xCB 0x73 0xFC 0xD9 0x0E 0xE0 0x57 0x74 0x22 0x2D 0xC0 0x67 0xFB 0x68 
      shift :  0x3B 0xD9 0x22 0x68 0xFC 0x74 0xFB 0x73 0x57 0x67 0xCB 0xE0 0xC0 0x59 0x0E 0x2D 
        mix :  0x4C 0x9C 0x1E 0x66 0xF7 0x71 0xF0 0x76 0x2C 0x3F 0x86 0x8E 0x53 0x4D 0xF2 0x56 
        add :  0xFA 0x63 0x6A 0x28 0x25 0xB3 0x39 0xC9 0x40 0x66 0x8A 0x31 0x57 0x24 0x4D 0x17 
       subs :  0x2D 0xFB 0x02 0x34 0x3F 0x6D 0x12 0xDD 0x09 0x33 0x7E 0xC7 0x5B 0x36 0xE3 0xF0 
      shift :  0x2D 0x6D 0x7E 0xF0 0x3F 0x33 0xE3 0x34 0x09 0x36 0x02 0xDD 0x5B 0xFB 0x12 0xC7 
        mix :  0x63 0x85 0xB7 0x9F 0xFC 0x53 0x8D 0xF9 0x97 0xBE 0x47 0x8E 0x75 0x47 0xD6 0x91 
        add :  0x24 0x72 0x40 0x23 0x69 0x66 0xB3 0xFA 0x6E 0xD2 0x75 0x32 0x88 0x42 0x5B 0x6C 
       subs :  0x36 0x40 0x09 0x26 0xF9 0x33 0x6D 0x2D 0x9F 0xB5 0x9D 0x23 0xC4 0x2C 0x39 0x50 
      shift :  0x36 0x33 0x9D 0x50 0xF9 0xB5 0x39 0x26 0x9F 0x2C 0x09 0x2D 0xC4 0x40 0x6D 0x23 
        mix :  0xF4 0xBC 0xD4 0x54 0x32 0xE5 0x54 0xD0 0x75 0xF1 0xD6 0xC5 0x1D 0xD0 0x3B 0x3C 
        add :  0xC8 0x16 0x77 0xBC 0x9B 0x7A 0xC9 0x3B 0x25 0x02 0x79 0x92 0xB0 0x26 0x19 0x96 
       subs :  0xE8 0x47 0xF5 0x65 0x14 0xDA 0xDD 0xE2 0x3F 0x77 0xB6 0x4F 0xE7 0xF7 0xD4 0x90 
      shift :  0xE8 0xDA 0xB6 0x90 0x14 0x77 0xD4 0x65 0x3F 0xF7 0xF5 0xE2 0xE7 0x47 0xDD 0x4F 
        mix :  0x98 0x16 0xEE 0x74 0x00 0xF8 0x7F 0x55 0x6B 0x2C 0x04 0x9C 0x8E 0x5A 0xD0 0x36 
        add :  0xC6 0x2F 0xE1 0x09 0xF7 0x5E 0xED 0xC3 0xCC 0x79 0x39 0x5D 0x84 0xF9 0xCF 0x5D 
       subs :  0xB4 0x15 0xF8 0x01 0x68 0x58 0x55 0x2E 0x4B 0xB6 0x12 0x4C 0x5F 0x99 0x8A 0x4C 
      shift :  0xB4 0x58 0x12 0x4C 0x68 0xB6 0x8A 0x01 0x4B 0x99 0xF8 0x2E 0x5F 0x15 0x55 0x4C 
        mix :  0xC5 0x7E 0x1C 0x15 0x9A 0x9B 0xD2 0x86 0xF0 0x5F 0x4B 0xE0 0x98 0xC6 0x34 0x39 
        add :  0xD1 0x87 0x6C 0x0F 0x79 0xC4 0x30 0x0A 0xB4 0x55 0x94 0xAD 0xD6 0x6F 0xF4 0x1F 
       subs :  0x3E 0x17 0x50 0x76 0xB6 0x1C 0x04 0x67 0x8D 0xFC 0x22 0x95 0xF6 0xA8 0xBF 0xC0 
      shift :  0x3E 0x1C 0x22 0xC0 0xB6 0xFC 0xBF 0x76 0x8D 0xA8 0x50 0x67 0xF6 0x17 0x04 0x95 
        mix :  0xBA 0xA0 0x3D 0xE7 0xA1 0xF9 0xB5 0x6E 0xD5 0x51 0x2C 0xBA 0x5F 0x41 0x4D 0x23 
        add :  0xFD 0xE3 0xBA 0xD2 0x05 0xE5 0xD0 0xD7 0x35 0x47 0x96 0x4E 0xF1 0xFE 0x37 0xF1 
       subs :  0x54 0x11 0xF4 0xB5 0x6B 0xD9 0x70 0x0E 0x96 0xA0 0x90 0x2F 0xA1 0xBB 0x9A 0xA1 
      shift :  0x54 0xD9 0x90 0xA1 0x6B 0xA0 0x9A 0xB5 0x96 0xBB 0xF4 0x0E 0xA1 0x11 0x70 0x2F 
        mix :  0xE9 0xF7 0x4E 0xEC 0x02 0x30 0x20 0xF6 0x1B 0xF2 0xCC 0xF2 0x35 0x3C 0x21 0xC7 
        add :  0xBD 0x6E 0x7C 0x3D 0xF2 0xB5 0x77 0x9E 0x0B 0x61 0x21 0x6E 0x8B 0x10 0xB6 0x89 
       subs :  0x7A 0x9F 0x10 0x27 0x89 0xD5 0xF5 0x0B 0x2B 0xEF 0xFD 0x9F 0x3D 0xCA 0x4E 0xA7 
      shift :  0x7A 0xD5 0xFD 0xA7 0x89 0xEF 0x4E 0x27 0x2B 0xCA 0x10 0x0B 0x3D 0x9F 0xF5 0x9F 
        add :  0x69 0xC4 0xE0 0xD8 0x6A 0x7B 0x04 0x30 0xD8 0xCD 0xB7 0x80 0x70 0xB4 0xC5 0x5A 
     output :  0x69 0xC4 0xE0 0xD8 0x6A 0x7B 0x04 0x30 0xD8 0xCD 0xB7 0x80 0x70 0xB4 0xC5 0x5A
```

## Getting started
Clone the repo
```bash
$ git clone https://github.com/A-Rain-Lover/AES-128.git
```
Compile using
```bash
$ make all
```
Run the tests
```bash
$ ./bin/tests
```

## References
* [AES specification in the original FIPS 197 publication](https://csrc.nist.gov/publications/detail/fips/197/final)