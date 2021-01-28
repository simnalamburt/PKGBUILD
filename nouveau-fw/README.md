nouveau-fw
========
Required firmwares to use hardware video acceleration with Nouveau.

```bash
# You only need to do it once
sudo pacman-key -r 0F85F46EE242057F
sudo pacman-key --lsign-key 0F85F46EE242057F

# Install
sudo pacman -U https://i.hyeon.me/PKGBUILD/nouveau-fw-340.108-1-any.pkg.tar.zst
```

#### References
- https://nouveau.freedesktop.org/VideoAcceleration.html#firmware
- https://wiki.archlinux.org/index.php/Hardware_video_acceleration#NVIDIA
