# z490
MSI z490m Gaming Edge Hackintosh
OpenCore-based EFI

# Hardware:
- MSI z490m Gaming Edge
- Intel i7-10700 (non-k)
- XFX RX590 Fatboy (no bios flash required)
- Patriot Viper 4 Blackout 16 GB (8x2)

# BIOS Settings:
- To be finalized

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

# Other notes:
- Ram is unstable when clocked to 3333Mhz (3200 XMP works though)
- i7-10700 CPU clocked with power limits removed reaches 72C @ 75F ambient during R20 with score of 4826
- Clocking the CPU to 102.9Mhz yields slightly higher speed for CPU and ram (around 3300Mhz) and appears to also run stable
- RX590 works without any special setup and runs relatively cool at around 50-50C at idle
- CPU at idle runs around 30-40C @ 70-80F ambient
