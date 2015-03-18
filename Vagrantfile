# -*- coding: utf-8 -*-
# -*- mode: ruby -*-
# vi: set ft=ruby :
#
# 2015-03-15
# github.com/mckaydavis
# STM32F0 Discovery Toolchain

VAGRANTFILE_API_VERSION = "2"


Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|
  #config.vm.box = "bionix/debian-wheezy-amd64"

  # The PPA that provides 'gcc-arm-none-eabi' doesn't play
  # nice with Debian 7. Settling for Ubuntu 14.10 LTS for now
  config.vm.box = "larryli/utopic64"

  config.vm.box_check_update = false

  config.vm.provision "shell", path: "provision-ubuntu.sh"

  config.vm.provider :virtualbox do |vb|
    # vb.gui = true

    # Note: VirtualBox needs the non-free Oracle Extension Pack
    # to bridge USB from the host to the VM.
    #
    # Download URL:
    # https://www.virtualbox.org/wiki/Downloads
    #
    # install command:
    # sudo VBoxManage extpack install Oracle_VM_VirtualBox_Extension_Pack-*.vbox-extpack

    # Enable USB 2.0
    vb.customize ["modifyvm", :id, "--usb", "on"]
    vb.customize ["modifyvm", :id, "--usbehci", "on"]

    # Enable the VirtualBox USB filter for the STM32F0 device
    vb.customize ["usbfilter", "add", "0", "-target", :id, "-name", "stm32F0", "-vendorid", "0x0483", "-productid", "0x3748"]
  end

end
