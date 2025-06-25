ECU BIN ↔ HEX Converter
=======================

This tool allows you to convert automotive ECU binary files (.bin) into Intel HEX format (.hex) and vice versa.

-------------
Usage (Windows)
-------------
1. Make a folder and save the script `ecu_converter.py` inside it.
2. Place the .BIN or .HEX file you want to convert into the same folder.
3. Open Command Prompt
4. Navigate to the folder containing the files:
   cd C:\path\to\folder

5. To convert .BIN → .HEX:
   python ecu_converter.py input.bin output.hex --base 0x08000000

6. To convert .HEX → .BIN:
   python ecu_converter.py input.hex output.bin --reverse
7-After executing this script converted file will be shown in the same folder .
Note:
- Replace "input.bin"/"input.hex" with your actual file names.
- Base address is optional (default = 0x00000000).
- Make sure you have Python  installed.
- This script does not require any external libraries.

-------------

Example Commands
-------------

BIN to HEX:
python ecu_converter.py my_ecu.bin my_ecu.hex --base 0x08000000

Sample Output 
✓ Successfully converted testing.bin to testing.hex
  Binary size: 4,194,304 bytes
  Base address: 0x08000000

HEX to BIN:
python ecu_converter.py my_ecu.hex recovered_ecu.bin --reverse

Sample Output
✓ Successfully converted testing.hex back to recovered_ecu.bin
  Address range: 0x08000000 - 0x083FFFFF
  Binary size: 4,194,304 bytes
