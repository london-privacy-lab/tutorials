#Setting up Yubikey 4 on Arch Linux

Documentation seemed to be all over the place. Compiling this file to archive for myself, to potentially present at a future Privacy Lab event, and equally to assist others seeking the same information.

1. Open a terminal and enter `sudo pacman -Sy`
2. Enter your password
3. `sudo pacman -S pcsc-tools yubikey-personalization-gui libu2f-host`
4. `echo 'KERNEL=="hidraw*", SUBSYSTEM=="hidraw", MODE="0664", GROUP="users", ATTRS{idVendor}=="2581", ATTRS{idProduct}=="f1d0"' | sudo tee /etc/udev/rules.d/10-security-key.rules`
5. reboot
6. [Optional Step] In Firefox you will need to add [this extension](https://addons.mozilla.org/en-US/firefox/addon/u2f-support-add-on/). U2F is expected in a future version. as of 20170218 there is a [live bounty](https://www.bountysource.com/issues/10401143-implement-the-fido-alliance-u2f-javascript-api/) if you're a Javascript Developer who could help implement the FIDO U2F API
7. **Open the 'Yubikey Personalization Tool'**
8. Insert your Yubikey
9. You should see in the top right text change from `No Yubikey inserted` to `Yubikey is inserted`
10. Your Yubikey has 2 slots for data. Mine came with just 1 installed. I wanted to create my own, so..
11. **To regenerate the OTP configuration**
11. In the menu select `Yubico OTP` to edit the One Time Password preferences
12. Select `Quick`
13. Select `Configure Slot 1` [The OTP *must* be in slot 1]
14. Select `Regenerate` [to create new OTP parameters]
15. Select `Write Configuration`
16. You will be given the option to backup these changes to a CSV file [we'll lock this with a secure password later]. You do not have to do this, but having lost GPG key access in the past, I highly recommend you do
17. **Now you'll [optionally] upload to the Yubico website**
18. Select `Upload to Yubico` [this will open the form in your default browser]
20. In the website form enter your email address
21. Back in the 'Yubico Personalization Tool' you'll see 4 fields needing to be copied over: `Serial Number` the Dec Number over in the far right, In parameters `Public Identity`, uncheck the `Hide Values` checkbox, copy over `Private Identity`, and finally `Secret Key`. *note that this website form does not like spaces*. Remove to avoid errors!
22. Click inside the `OTP from the Yubikey` and manually press the button on your Yubikey
23. Enter the Captcha
24. Select `Upload AES key`
25. `Success! Key upload successful`
26. **Now [optionally] edit the static password**
27. Back in 'Yubico Personalization Tool' select `Static Password` from the menu
28. Select `Advanced` [not sure about you but I wanted this really strong]
29. Select `Configuration Slot 2`
30. Select `Yubikey unprotect - enable protection`
31. Select `New Access Code` and checkbox `New Access Code/Use Serial Number` [you can double check by removing the key and see the number is the same with a few preceeding 0's]
32. Select `Password Parameters` to your needs [I selected checkboxes for `upper an lower case`, `Alphanumeric`, and finally `Generate` for all 3 fields here]
33. Select `Write Configuration` [this will also save to your earlier created CSV]

**To find out more about the 'Yubico Personalization Tool'** [click here](https://www.yubico.com/support/knowledge-base/categories/articles/yubikey-personalization-tool-users-guide/) for the manual

**To test out your Yubikey** [click here](https://demo.yubico.com/) to head over to the demo site

**To zip your CSV file with a strong password** `zip -P 'y0ur_cr@zy_pa$$w0rd' -r new_zip_name.zip Yubikey_backup.csv` [of course make this super strong. I used [KeePassX2](https://www.archlinux.org/packages/community/x86_64/keepassx2/) to generate one. Be sure to backup your KeePassX2 database!]
