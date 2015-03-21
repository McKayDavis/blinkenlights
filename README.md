# Social BlinkenLights #

## ACHTUNG!

ALLES TURISTEN UND NONTEKNISCHEN LOOKENPEEPERS!
DAS KOMPUTERMASCHINE IST NICHT FÜR DER GEFINGERPOKEN UND MITTENGRABEN! ODERWISE IST EASY TO SCHNAPPEN DER SPRINGENWERK, BLOWENFUSEN UND POPPENCORKEN MIT SPITZENSPARKEN.
IST NICHT FÜR GEWERKEN BEI DUMMKOPFEN. DER RUBBERNECKEN SIGHTSEEREN KEEPEN DAS COTTONPICKEN HÄNDER IN DAS POCKETS MUSS.
ZO RELAXEN UND WATSCHEN DER BLINKENLICHTEN.

### Requirements

* [VirtualBox 4.3.18](http://download.virtualbox.org/virtualbox/4.3.18/)
* [Vagrant 1.7.2](http://www.vagrantup.com/download-archive/v1.7.2.html)

### Status

* The VM is configured to provide capabilities to compile, flash, and debug the STMD32F0-Discovery evaluation board.  (http://www.st.com/stm32f0discovery)

* Currently, Vagrant/VirtualBox on the host must be run as superuser to allow VirtualBox to bridge the USB port to the VM.

* Also, commands inside the VM that communicate with the board via USB (e.g. `st-flash`)must also be run as superuser.

* Before running `sudo vagrant up` VirtualBox needs the non-free Oracle Extension Pack to bridge USB from the host to the VM.
  * Download the extension via: `curl -fSL http://download.virtualbox.org/virtualbox/4.3.18/Oracle_VM_VirtualBox_Extension_Pack-4.3.18.vbox-extpack -o /tmp/Oracle_VM_VirtualBox_Extension_Pack-4.3.18.vbox-extpack`
  * Install via: `cd /tmp && sudo VBoxManage extpack install Oracle_VM_VirtualBox_Extension_Pack-*.vbox-extpack`

### Changelog
* v0.1 - 2015-03-16 - Vagrantfile to create the STM32F0 Discovery toolchain on Ubuntu 14.10 amd64
