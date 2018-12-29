## WASM (WebAssembly)

Keyword files are stored in binary format. In order to use them within a JavaScript environment you need to convert them to a `Uint8Array`. You may use any tool to read the keyword file byte by byte. On a Linux box you may use `xxd` utility. For example

```bash
xxd -i -g 1 resources/keyword_files/wasm/americano_wasm.ppn
```

Gives

```bash
unsigned char resources_keyword_files_wasm_americano_wasm_ppn[] = {
  0xd3, 0x15, 0x92, 0xe5, 0x38, 0x1b, 0xff, 0x28, 0xa3, 0x5f, 0x62, 0x82,
  0x39, 0x0e, 0x82, 0x14, 0xd0, 0xaf, 0x93, 0xcf, 0xa9, 0xa9, 0xbc, 0x3e,
  0x01, 0x9e, 0x89, 0xd6, 0x43, 0x45, 0x34, 0xec, 0x5b, 0x3e, 0xb0, 0x5b,
  0xae, 0xd8, 0xaa, 0xa4, 0xc3, 0x27, 0x79, 0x39, 0xa2, 0xc5, 0x58, 0x74,
  0x12, 0x88, 0x2d, 0xbf, 0x5d, 0x3d, 0xbc, 0xc0, 0xd3, 0x20, 0xf3, 0xef,
  0x8d, 0xae, 0xb5, 0xb7, 0x12, 0xfe, 0x27, 0xab, 0x30, 0x5d, 0x8e, 0xb9,
  0x03, 0x3d, 0xb2, 0xe3, 0x3b, 0xe0, 0x39, 0xfe, 0x1f, 0xc6, 0xee, 0xcc,
  0x44, 0x9f, 0x43, 0xc9, 0xdc, 0xe8, 0xcb, 0x81, 0xc1, 0x45, 0x81, 0xd1
};
```

Then, the array can be used in JavaScript.
