# IAPPatcher

IAPPatcher is a program that patches any apk to bypass the billing process (In-App Purchases).

### How does it work?

There is an IPC-like communication between the application and the com.android.vending process.

I hooked the sender (to get the details of the order) and the receiving handler (to fake a success transaction).

Also I am deleting the Google library transaction signature verifier.

It won't work on every app (most apps will verify the purchase with the server) but it is supposed to work on most of the offline apps and in particular - games.

## Requirements
1. Python3
2. Java installed

## Installation

```bash
git clone https://github.com/BarburONet/IAPPatcher.git
```
Requirements installation:
```bash
pip install -r requirements.txt
```
## Usage

```bash
python iappatcher_patcher/main.py -p ./to_patch.apk
```

## References
- Nice repo that helped me understand the mechanism: [billing-hack](https://github.com/Techbrunch/billing-hack)
- Article about this topic: https://www.securingapps.com/blog/BsidesLisbon17_AbusingAndroidInappBilling.pdf


## Disclaimer

For educational purposes only of course ;)
