+++
author = "Vladimir Likhanov"
title = "Creating a bootable USB stick for Ubuntu 22.04 LTS"
date = "2022-10-02"
description = "Creating a bootable USB stick for Ubuntu 22.04 LTS"
featured = true
tags = [
    "Ubuntu"
]
categories = [
    "Linux",
]
thumbnail = "images/blog/linux/ubuntu-logo.png"
+++

> This post shows you how to create a bootable USB stick for Ubuntu 22.00 LTS. You can then use this UBS stick
to install the Ubuntu distribution on your laptop.

By creating a bootable USB stick, you can install the Ubuntu distribution on your laptop or try it out in Live mode.

> **NOTE**: In this tutorial, we'll create a bootable USB stick using a 4 GB or larger USB stick. The USB stick should be empty as all data on it will be erased.

## Downloading an ISO image

First of all, we need to download the right Linux distribution. As we’ll be creating a bootable USB stick for Ubuntu 22.04 (the latest Ubuntu LTS version at the time of this writing), we need to download the ISO image for this distribution:

1. Go to the [Ubuntu website](https://ubuntu.com/download/desktop).

2. Click on the **Download** button.

![Ubuntu - downloading the ISO image](/images/blog/linux/ubuntu-downloading-iso-image.png)

3. Follow the on-screen instructions to download the ISO image to your laptop.

## Writing the ISO image to a USB stick

We’ll use the Rufus utility to write the downloaded ISO file to a USB stick. This utility is available for
most modern operating systems (e.g., Windows and Mac). 

1. Go to the [Rufus](https://rufus.ie/) website and download the utility.

2. Double-click on the installation file and follow the on-screen instructions to install the utility on your laptop. You can also download a portable version of this utility and skip this step.

3. Launch the utility.

![Ubuntu - starting the Rufus utility](/images/blog/linux/ubuntu-launching-rufus-utility.png)

4. In the **Device** field, select your USB stick. Make sure that you’ve selected the correct USB stick, as all data will be erased on this stick.

5. Ensure that the **Disk or ISO image** entry is selected in the **Boot selection** field.

6. Click on the **SELECT** button and navigate to the downloaded Ubuntu ISO image.

7. Once you’ve selected the ISO image, Rufus automatically fills out all the remaining fields and activates the **START** button. So, your window may look like the following:

![Ubuntu - configuring drive settings in Rufus](/images/blog/linux/ubuntu-launching-rufus-utility.png)

8. Click on the **START** button.

9. If you see the **ISOHybrid image detected** window, make sure that the **Write in ISO Image mode (Recommended)** option is selected and click **OK**.

![Ubuntu - displaying the warning windows](/images/blog/linux/ubuntu-rufus-warning-window.png)

10. In the displayed warning window, click **OK** to confirm the operation.

11. Wait for Rufus to finish creating the bootable USB stick.

![Ubuntu - progress bar in Rufus](/images/blog/linux/ubuntu-rufus-progress-bar.png)

12. Once the writing process is complete, click on the **CLOSE** button.

## Checking the bootable USB stick

Now we need to check that the created USB stick can be booted:

1. Insert the USB stick into your laptop.

2. Reboot the laptop.

3. When your laptop starts up again, press the BIOS setup key (usually F2 or F12, depending on your laptop hardware).

4. In the BIOS menu, go to the Boot section and select your USB drive as the preferred boot media.

5. Reboot your laptop once more. Now the laptop should boot from the selected USB drive, and you should see the Ubuntu installation welcome screen.