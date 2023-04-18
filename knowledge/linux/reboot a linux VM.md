To reboot a Linux virtual machine (VM), you can follow these steps:

1.  Open a terminal window on the Linux VM.
2.  Type the following command: `sudo reboot`
3.  Press Enter.
4.  Enter the administrative password if prompted.
5.  Wait for the VM to shut down and restart.

Alternatively, you can use the following command to force the VM to reboot immediately without waiting for any running processes to complete:

```bash
sudo reboot -f
```

It is recommended to save any unsaved work and close any running applications before rebooting a VM.