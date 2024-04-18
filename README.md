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
  -Steam
  -Discord
  -Base-devel
  -acpi_call
  -Modrinth-app
  
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


    Subreddit Icon
r/linux
•Posted by
u/mort96
6 years ago
PSA for Firefox users: set MOZ_USE_XINPUT2=1 to enable macOS-like smooth scrolling

Firefox scrolling fix from reddit:

I've been annoyed for a while that Firefox only supports the kind of two finger scrolling where moving the fingers on the touch pad a decent amount emits a scroll wheel event. I just now found out that if you start Firefox with the environment variable MOZ_USE_XINPUT2 set to 1, it will use xinput 2, and support actual smooth touch pad scrolling.

I know this works for Firefox 55 or newer, but don't know the earliest version which supports it. I assume it will be enabled by default at some point, but it isn't yet in Firefox 58 (the current nightly).

    Run this command:

    echo export MOZ_USE_XINPUT2=1 | sudo tee /etc/profile.d/use-xinput2.sh

    Log out and back in.

    Firefox should now use xinput 2.

    (optional) Open Firefox and go to about:preferences -> Advanced (or about:preferences -> Browsing for Firefox Nightly), and uncheck "Use smooth scrolling". This disables the old style "smooth scrolling", which just causes an annoying delay when using xinput2 style scrolling imo.
