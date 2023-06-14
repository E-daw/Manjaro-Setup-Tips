# Manjaro-Setup-Tips
This is a small guide dedicated on how I set up my linux installation across different PCs


Latest stable kernel
Manjaro KDE Plasma
-check archlinux.org on how to set laptop up specifically

-for amd systems, enable amd-pstate

Applications to install:
  -Autocpu-freq
  -manjaro-pipewire
  -power-profiles-daemon
  -optimus-manager-qt
  -laptop-mode
  
Paths to rem:
  
  
Settings to change:
  Enable network printer discovery https://wiki.manjaro.org/index.php/Printing
    -Enable cups in systemctl
    -enable avahi-daemon.service
  Fix SSH on VPN
    sudo ip li set mtu 1200 dev wlan0
  

Environmental Variables:
  -VK_ICD_FILENAMES=/usr/share/vulkan/icd.d/radeon_icd.i686.json:/usr/share/vulkan/icd.d/radeon_icd.x86_64.json steam
    This forces the use of integrated graphics. Sometimes steam games run through proton will select the nvidia graphics by default because of DXVK.
