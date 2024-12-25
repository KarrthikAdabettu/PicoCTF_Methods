## Approach :

1. First, copy the file and use `wget` to download it into your directory. Then, unzip the folder.

2. Inside the extracted folder, navigate to the "drop-in" folder located at the very end. Inside this folder, you’ll find a `.png` file containing a QR code.

3. To decode the QR code, you can either:
- Use a mobile phone to scan the QR code.
- Use the tool `zbarimg` in Kali Linux to decode the QR code directly in your terminal.

4. To use `zbarimg`, follow these steps:
- Update your system:
  ```
  sudo apt-get update
  ```
- Install `zbar-tools`:
  ```
  sudo apt install zbar-tools
  ```
- Decode the QR code with:
  ```
  zbarimg flag.png
  ```

The decoded output will show the flag.

5. The flag is:  picoCTF{p33k_@_b00_d4ca652e}


### Notes :
- Ensure you run `sudo apt-get update` before installing `zbar-tools` to avoid any installation errors.
