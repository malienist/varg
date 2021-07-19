# varg
Decryptor tool for AES-encrypted payloads

![alt text](https://github.com/vithakur/varg/images/varh.png)

## What is Varg?
Varg is a tool written in PowerShell that helps you decrypt data that has been encrypted using AES encryption. The most common application we see in the cyberSec world is malicious scripts that are dropped on victim machines in the for of encrypted payloads that execute malicious code once decrypted.

## Usage
You’ll need to first extract the encrypted payload from the first stage malware (usually a vbs/js) and save it as a text file. Absolute path of this file will need to be passed to the tool along with the key and it’ll decrypt the payload and save the decrypted file as ‘decrypted.txt’ in the current directory.
## Step-by-step:
Save the encrypted data in a text file as 'encrypted.txt' in the current dir.
Run the tool (double-click).
Provide the key (in the full form, eg. 1,2,3,4,5,6,7,8,9,10,11,12,13,14,15,16).
The decrypted payload is saved in the current dir as 'decrypted.txt'.
All done.

## The Key Length
If you’re wondering where do you get the key length from, it’s a valid question, albeit with a simple answer. The malware writer has to include the key in the dropper for the the code to run successfully. The code simply wouldn’t run without it. So usually, they include the key right in the end, after the encrypted payload. They make sure its not very obvious to spot but nonetheless, it is there. Something like this: -k (1..16).

Complete details in this post - https://malienist.medium.com/varg-payload-decryptor-c5887a50b36e
