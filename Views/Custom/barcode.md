# Barcode

**Description**

A view that generates and displays a barcode or QR code.

**Parameters**

- `barcodeType`: The type of barcode to generate. Supported values: `qr`, `aztec`, `pdf417`, `code128`.
- `foregroundColor`: The color of the barcode, in hex format.
- `backgroundColor`: The color of the background, in hex format.
- The text content of the tag is the string to encode.

**Example**

```xml
<body>
    <barcode barcodeType="qr" foregroundColor="#0000FF" backgroundColor="#FFFFFF">Hello, World!</barcode>
</body>
```

<img src="/Screenshots/Views/Custom/barcode_1.png" width="250" alt="Screenshot">
