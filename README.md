Centos Kickstart
================

Install centos without any prompts.

1. Download the ks.cfg file.
   Replace the root and st user passwords with better ones.
2. Start a server running on the local network that serves the new ks.cfg file.
   Start the local server in the same directory where you downloaded the ks.cfg

```
ruby -run -e httpd . -p 8000
```

3. Plug in the usb drive with the centos min iso
4. Restart PC
5. Press F12 when BIOS loads to go to the boot menu
6. Select the USB device in the boot menu
7. The centos min iso will boot
8. Press esc
9. At the `boot:` prompt type:

```
linux ks=http://192.168.1.3:8000/ks.cfg
```

10. Press enter and :)
