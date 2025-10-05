# BarcodeScanner

**Description**

A view that uses the device's camera to scan for barcodes.

**Parameters**

- `key`: A key to store the scanned barcode data. The data will be a dictionary with `text` and `type` keys.
- `rectColor`: The color of the rectangle drawn around the detected barcode, in hex format.
- `rectWidth`: The width of the rectangle's border.

**Example**

```xml
<body>
    <zstack>
        <barcodescanner key="scannedCode"/>
        <text if="$scannedCode.text != ''" background="black.opacity(0.5)" foregroundColor="white" padding="10">
            Scanned: $scannedCode.text (Type: $scannedCode.type)
        </text>
    </zstack>
</body>
```
<img src="/Screenshots/Views/Custom/barcodescanner_1.png" width="250" alt="Screenshot">
