# Encrypto

Encrypto is a simple js script for encoding and decoding a BIP39 recovery phrase to/from a decimal/hex number.

Encrypto converts your BIP39 recovery phrase into a number which can be easily stored in plain sight. 

## Why

People go to extreme lengths to keep their BIP39 recovery keys secure. They must be stored permanently, while also kept hidden. 

The problem is, if you find someone's BIP39 recovery phrase, e.g. 24 random words from a 2000 word dictionary, it's pretty obvious what it is! 

## How it works

Encrypto uses the [ChanceJS](https://chancejs.com/) javascript library to repeatably shuffle (reorder) the BIP39 word list. Shuffling using the same encryption key will always produce the same order.

The number outputted is a sequence of the 4-digit locations of each word. The number is also provided in hex format as an alternative.

For example:
The seed phrase `adapt add addict` with the password `123` produces `017717401793`.

In other words, when shuffling the word list with the password `123`, the word `adapt` is in position 177, `add` is in position 1740, and `addict` is in position 1793.

## Usage

1. Visit [https://jpalmerx.github.io/encrypto/](https://jpalmerx.github.io/encrypto/) to use the tool.
2. Enter the BIP39 recovery phrase you'd like to encode, and an encryption key (password).
3. Safely store the resulting decimal *OR* hex number.
4. Decode the number back to a BIP39 recovery phrase by entering it into the form and using the same encryption key.

## Notes

Encrypto uses vanilla javascript and executes locally in the browser. It does not require an internet connection to run, and does not connect to a server or store any information entered.

All encoding/decoding is designed to be 100% repeatable. 

## Feedback
Feedback is welcome! This was just a simple thought I had one day. Please let me know what you think!

## License
[MIT](https://choosealicense.com/licenses/mit/)
