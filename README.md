# TODO

- [ ] Set timezone
- [ ] Add user programatically
- [ ] Configure DNS? -- maybe later, after the exam...
- [ ] GDM appearance
- [ ] Cedilla
- [ ] Configure Laptop's touchpad
- [ ] Obsidian
- [ ] Discord
- [ ] Gimp
- [ ] Devel tools:
  - [ ] awscli
  - [ ] redis-tools
  - [ ] docker
  - [ ] docker-compose
  - [ ] vscode
  - [ ] font-jetbrains-mono
  - [ ] default-jre
  - [ ] default-jdk

# Notes

- Role python may not be required since Kali 2022.1 (verify it)
- Set volume output device to HDMI on Desktop -- can be done via dconf
- Keyboard role:
  - Set `KEYMAP=y` in `/etc/initramfs-tools/initramfs.conf`
  - Then update kernel image? `update-initramfs -u`? See: https://wiki.debian.org/Keyboard
