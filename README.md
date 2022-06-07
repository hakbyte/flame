# Flame

Flame is a set of Ansible roles organized as a playbook that I use manage my
laptop and workstation with [Kali Linux](https://www.kali.org/). I got the
inspiration from [spark](https://github.com/pigmonkey/spark) and that's why it's
called *Flame*.

> :memo: You may also want to check out my [dotfiles](https://github.com/hakbyte/dots)
> to further customize your brand new Kali installation.

# Usage

> :warning: **Important:**
> - This playbook assumes you have a default installation of Kali Linux
> 2022.2 with Gnome as the Desktop Environment
> - Before running the playbook, read the *Customization* section to adapt it
> to your environment

Install dependencies:

```
$ sudo apt-get update
$ sudo apt install ansible python3-psutil
```

Clone this repository:

```
$ git clone https://github.com/hakbyte/flame.git
$ cd flame
$ ansible-playbook -i hosts playbook.yml -e target=<TARGET> -K
```

You will be prompted for the root password (*BECOME* password in Ansible
parlance) before proceeding.

> :memo: Possible values for `<TARGET>` are `desktop` and `laptop`. The former
> is fine tuned for a smaller screen (1920x1080 pixels) besides configuring the
> touchpad.

# Customization

It's expected that you update `var/all.yml` and `tasks/pretasks.yml` to set
the following values:

- Hostname (one for each `<TARGET>`)
- Default username and password
- Locale
- Timezone
- Keyboard layout
- Nameservers (for DNS resolution)

> :warning: **Important:** the `desktop` target is configured to install the
> Nvidia proprietary drivers. To avoid installing these, run the playbook with
> `--skip-tags nvidia`.

# TODO

- [ ] Add user programmatically
- [ ] Fine tune GDM appearance
- [ ] Let user choose betwen GDM and LightDM
- [ ] Initialize Metasploit: `sudo msfdb init`
- [ ] Set volume output device to HDMI on Desktop (can it be done via dconf?)
- [ ] Fix Bitwarden installation (*.deb package not available anymore on Github?) -- maybe install it using Flatpak or AppImage?
- [ ] Switch to LightDM due to keyboard layout issue? References:
  - https://gitlab.gnome.org/GNOME/gdm/-/issues/462
  - https://gitlab.gnome.org/GNOME/gdm/-/issues/459
- [ ] Set `/etc/vconsole.conf` to `us-acentos` for instance
- [ ] Add *Features* section to `README.md`
- [ ] Add *Security* section to `README.md`
- [ ] Enable sudo without password for some commands (:warning: document security concerns):
  - [ ] nmap
  - [ ] openvpn
