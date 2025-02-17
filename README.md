# CURRENTLY NOT FUNCTIONING; I would love to know what I'm missing, help massively appreciated
* Does waydroid overlay files require specific permissions?
* Should it be setting waydroid props a different way, like through a config file?
* Is there more that needs to be done as well as setting props and copying overlay files?
* What enviroment is necessary for setting waydroid props?
* Are the props intended to be prefixed with "persist." to stay active after the waydroid session restarts?
# waydroid-libndk

Simplifies installation of arm translation for waydroid

### Arch/Arch based:
```sh
cd /tmp && git clone https://github.com/Elec3137/waydroid-libndk && cd ./waydroid-libndk && makepkg -si
```
