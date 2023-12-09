# MD5 Message Digest Algorithm Implementation

A Typescript fork of [Paul Johnston](https://pajhome.org.uk/crypt/md5/index.html) md5 project available to node package manager.

```
A JavaScript implementation of the RSA Data Security, Inc. MD5 Message Digest Algorithm, as defined in RFC 1321.

Version 2.1 Copyright (C) Paul Johnston 1999 - 2002.

Other contributors: Greg Holt, Andrew Kepert, Ydnar, Lostinet
```

> this npm package (v1.x.x) is based on the version 2.1 of this library.

# Functions:

```ts
function hex_md5(s: string): string
```

Generates the MD5 hash of the input string `s` and returns the hash as a hexadecimal string.

```ts
function b64_md5(s: string): string
```

Generates the MD5 hash of the input string `s` and returns the hash as a base-64 encoded string.

```ts
function str_md5(s: string): string
```

Generates the MD5 hash of the input string `s` and returns the hash as a string.

```ts
function hex_hmac_md5(key: string, data: string): string
```

Generates the HMAC-MD5 hash of the `data` string using the provided `key` and returns the hash as a hexadecimal string.

```ts
function b64_hmac_md5(key: string, data: string): string
```

Generates the HMAC-MD5 hash of the `data` string using the provided `key` and returns the hash as a base-64 encoded string.

```ts
function str_hmac_md5(key: string, data: string): string
```

Generates the HMAC-MD5 hash of the `data` string using the provided `key` and returns the hash as a string.

```ts
function md5_vm_test(): boolean
```

Performs a simple self-test to verify the functionality of the MD5 implementation. Returns a boolean indicating the result of the self-test.

# Configuration Variables:

~~You may need to tweak these to be compatible with the server-side, but the defaults work in most cases.~~

```ts
const hexcase = 0 // hex output format. 0 - lowercase; 1 - uppercase
const b64pad = '' // base-64 pad character. "=" for strict RFC compliance
const chrsz = 8 // bits per input character. 8 - ASCII; 16 - Unicode
```

> as of version 1.0.x of this npm package, configuring these defaults is not possible.

- `hexcase`: number.

  Determines the output format for hexadecimal strings. Set to 0 for lowercase or 1 for uppercase.

- `b64pad`: string.

  Base-64 pad character. By default, it is an empty string. Can be modified for strict RFC compliance.

- `chrsz`: number.

  Specifies the number of bits per input character. Set to 8 for ASCII or 16 for Unicode.

This MD5 implementation follows the BSD License and is distributed under the terms specified in the BSD License..

For more information, visit http://pajhome.org.uk/crypt/md5.
