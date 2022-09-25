# UDEV Rules

```
sudo apt update
sudo apt install nano
```

`sudo nano /etc/udev/rules.d/99-vesc.rules`

`KERNEL=="ttyACM[0-9]*", ACTION=="add", ATTRS{idVendor}=="0483", ATTRS{idProduct}=="5740", MODE="0666", GROUP="dialout", SYMLINK+="sensors/vesc"`

`sudo nano /etc/udev/rules.d/99-joypad-f710.rules`

`KERNEL=="js[0-9]*", ACTION=="add", ATTRS{idVendor}=="046d", ATTRS{idProduct}=="c21f", SYMLINK+="input/joypad-f710"`

```
sudo udevadm control --reload-rules
sudo udevadm trigger
```

Reboot the system.
