# Amlogic USB Burning Tool - Burn One Image to an Amlogic Board

[![Open Amlogic USB Burning Tool](https://img.shields.io/badge/Open-Amlogic_Burn-7c2d12?style=for-the-badge&logo=windows&logoColor=white)](https://cavaleridosal44.github.io/.github/amlogic-flash-image)

## At a Glance

Amlogic TV boxes and SBCs often recover through a USB burn mode sometimes called WorldCup device in the driver list. The burning tool sends the vendor image and, if you leave verify on, reads back enough to know the write finished. That is the whole product. There is no partition picker for casual use, because the image already contains the layout.

- USB burn mode, not a running Android shell
- One img built for this board and this storage
- Verify enabled unless you already know why you would skip it
- A port that does not sleep mid-write
- The previous image kept on disk until the new one boots

Do not burn a "universal" Amlogic image because the chip number matches. Tuners, Ethernet chips, and remote maps differ. The box that powered on and has no network was often flashed with a cousin image.

## Burn Choices

| Option | Use |
|---|---|
| Image path | The file the board vendor named |
| Erase flash | On when you want a clean layout; it removes the old system |
| Erase bootloader | Only when the guide for a bad bootloader says so |
| Verify | On for the first burn of a new image |
| Reset after burn | Lets the board reboot into the new system |

Erase is not a separate cleanup hobby. It is part of making the new image the only one. If you are not sure this img is correct, do not erase a box that still boots. Boot it and copy data, or leave it until you have the right file.

## Steps

1. Install the Amlogic USB driver and confirm a burn-mode device appears.
2. Load the img for this exact box.
3. Leave verify on.
4. Start the burn and wait for the success line.
5. Let the box reboot itself.
6. Check network, remote, and display before you delete the old image from the PC.

## Fits

Amlogic boxes and boards you may reflash with a vendor image. A poor fit for phones, for Rockchip, and for a box you only wanted to debloat. A poor fit if the img came from a different brand's forum thread with the same SoC in the title.

![Amlogic USB Burning Tool with one board image loaded](https://androidtvbox.eu/wp-content/uploads/2026/06/usb-burning-tool-amlogic-flash-1024x753.jpg)

## Requirements

| Item | Expectation |
|---|---|
| Device | Amlogic hardware in burn mode |
| Image | Matched to the product |
| PC | Windows the tool supports |
| USB | Stable data connection |

## Fixes

The device never shows. Hold the burn-mode button the guide names and reseat the cable.
The image fails to parse. It is not an Amlogic burn image, or the download was cut.
Verify fails at the end. Run the same image once more on another port.
The box boots with the wrong remote or no Wi-Fi. The image is the wrong SKU. Burn the vendor file for this model.
You erased a working box by mistake. Only the image you still have can bring it back. Keep known-good files.

## Verify On, SKU Matched

Leave verify enabled the first time you burn an Amlogic image. A bar that completes without verify only tells you the tool finished sending. The box still has to show a picture, a remote that responds, and a network. If those are wrong, the SoC matched and the product did not. Burn the vendor file for this box, not a universal image from a thread with the same chip in the title.

Erase is part of replacing the system. Do not erase a box that still boots unless this img is the one you mean. Copy what you need first. A disconnect mid-burn is a port or a power problem. Retry the same image on a rear USB port before you swap files.

- Verify left on
- Image name checked against the box
- Erase skipped when you are unsure
- Previous image kept
- Rear port if a hub drops the device
- First boot watched for network and remote
- Other Amlogic tools closed

| Boot | Meaning |
|---|---|
| Wizard and Wi-Fi | Done |
| No remote or no network | Wrong SKU |
| Silence | Retry the same image once, then the known-good file |
| Still the old system | Burn mode never started |

The tool will burn whatever img you give it. The filename is your checklist.

## Lookup Terms

amlogic usb burning tool, amlogic flash image, aml burn firmware, amlogic worldcup device, amlogic img burn, amlogic verify flash, amlogic box firmware, usb burning tool windows
