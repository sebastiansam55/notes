# Protips
Do you use a *real* password when logging into your VMs? Is it a pain to type that in everytime because windows does not allow you to paste at the login screen? Boy do I have good news for you;

`vboxmanage controlvm VMNAME keyboardputstring "password"`

The above command as you may be able to guess will make virtualbox send keyboard input to the VM as if you were typing on the keyboard. There are also `keyboardputscancode` and `keyboardputfile` available as options.

Virtualbox has some of the best open source documentation you should check it out if you get a chance. There are a ton of features that are super obscure but super useful;
[https://www.virtualbox.org/manual/ch08.html](https://www.virtualbox.org/manual/ch08.html)