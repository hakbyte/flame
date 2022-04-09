# TODO

- [x] Set timezone
- [ ] Add user programatically
- [ ] Configure DNS? -- maybe later, after the exam...
- [ ] GDM appearance
- [x] Cedilla
- [ ] ~~Configure Laptop's touchpad~~
- [x] Obsidian
- [x] Discord
- [ ] Gimp
- [ ] Initialize Metasploit: `sudo msfdb init`
- [ ] Devel tools:
  - [x] awscli
  - [ ] ~~redis-tools~~
  - [x] docker
  - [x] docker-compose
  - [x] vscode
  - [x] font-jetbrains-mono
  - [ ] default-jre
  - [ ] default-jdk
- [ ] Install chrome and vscode via apt sources. Try the same for Tilix

# Notes

- Role python may not be required since Kali 2022.1 (verify it)
- Set volume output device to HDMI on Desktop -- can be done via dconf
- Keyboard role:
  - Set `KEYMAP=y` in `/etc/initramfs-tools/initramfs.conf`
  - Then update kernel image? `update-initramfs -u`? See: https://wiki.debian.org/Keyboard
