# wmbusmeters Telegram Decode Assignment

## Objective
Decode an OMS / wM-Bus encrypted telegram and extract meter data using `wmbusmeters`.

---

## Environment
- OS: Windows 10
- Linux: Ubuntu 22.04 (WSL2)
- Tool: wmbusmeters
- Meter type: Water meter (waterstarm)

---

## Input Data
- Encrypted wM-Bus telegram provided as hex string
- AES key provided for decryption

The raw telegram is saved in:

telegram.txt


---

## Decoding Command Used

```bash
wmbusmeters \
  --analyze=4255794d3dccfd46953146e701b7db68 \
  --format=json \
  a144c5142785895070078c20607a9d00902537ca231fa2da5889be8df3673ec136aebfb80d4ce395ba98f6b3844a115e4be1b1c9f0a2d5ffbb92906aa388deaa82c929310e9e5c4c0922a784df89cf0ded833be8da996eb5885409b6c9867978dea24001d68c603408d758a1e2b91c42ebad86a9b9d287880083bb0702850574d7b51e9c209ed68e0374e9b01febfd92b4cb9410fdeaf7fb526b742dc9a8d0682653


Decoding Result

Meter ID: 50898527

Meter type: Water

Total consumption: 4.48 m³

Meter timestamp: 2025-09-26 16:36

Status: OK

Historical monthly consumption values successfully decoded

The decoded JSON output is saved in:

decoded_output.json

Conclusion

The encrypted OMS/wM-Bus telegram was successfully decrypted using the provided AES key.
All relevant meter data including total consumption, historical values, timestamps, and status flags were extracted and validated using wmbusmeters.

This demonstrates correct handling of encrypted wM-Bus telegrams and JSON serialization of meter data.


