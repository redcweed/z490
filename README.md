# z490
MSI z490m Gaming Edge Hackintosh
OpenCore-based EFI

# Hardware:
- MSI z490m Gaming Edge
- Intel i7-10700 (non-k)
- XFX RX590 Fatboy (no bios flash required)
- Patriot Viper 4 Blackout 16 GB (8x2)

# BIOS Settings:
- Above 4GB MMIO BIOS Assignment: Enabled
- Internal Graphics: Enabled
- Fast Boot: Disabled
- Secure Boot Mode: Standard
- Wake Up Event By: OS
- Above 4G memory/Crypto Currency mining: Enabled
- IGD Multi-Monitor: Enabled
- Extreme Memory Profile(XMP): Enabled
- Intel Virtualization Tech: Disabled
- CFG Lock: Disabled
(Below are my system specific and can be ignored)
- Long Duration Power Limit: 95
- Short Duration Power Limit: 95
- CPU Fan1 type: PWM
- level 1 T: 30
- level 2 T: 50
- level 3 T: 60
- level 4 T: 75
- level 1 S: 38
- level 2 S: 65
- level 3 S: 90
- level 4 S: 100
- SYS Fan1 Smart Fan Control: ENabled
- SYS Fan1 type: PWM
- level 1 T: 30
- level 2 T: 50
- level 3 T: 60
- level 4 T: 70
- level 1 S: 50
- level 2 S: 68
- level 3 S: 90
- level 4 S: 100

# What Works:
- Sleep/Wake
- Shutdown
- Onboard Bluetooth
- 2.5G Ethernet (must use attached patched kext)
- Sound (via VoodooHDA kext for back panel, front panel, and HDMI output)
- iMessage
- Continuity/Handoff
- Quicksync hardware acceleration via iGPU
- All USB 3 and 2 ports
- Power management

# What Doesn't Work:
- Onboard Wifi ax card

# Odd items:
- AAPL: [EB|#LOG:EXITBS:START] error on startup until leveraged a boot patch included in the config.plist

# Other notes (mostly hardware-specific notes to self):
- 3200Mhz rated ram is unstable when clocked to 3333Mhz (3200 XMP works though)
- i7-10700 CPU clocked with power limits removed reaches 72C @ 75F ambient during R20 with score of 4826
- Clocking the CPU to 102.9Mhz yields slightly higher speed for CPU and ram (around 3300Mhz) and appears to also run stable
- RX590 works without any special setup and runs relatively cool at around 50-50C at idle
- CPU at idle runs around 30-40C @ 70-80F ambient
