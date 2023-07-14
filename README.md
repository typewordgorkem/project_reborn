# Project Reborn

## Part-I ( Vga-Bios update)

In this project, it is aimed to increase the 90-watt rtx2060 in my specific device to 115 watts by using the existing programs (throttlestop, nvflash) and to increase the 45w short power limit value of the i7-9750h processor to 65w and also to increase the 65w long power limit to 80w with the help of throttlestop. . A total performance increase was targeted and completed successfully.


## Warning!!!
-Graphics cards can come with different types of memory. In this context, if the current version is, for example, a card with Samsung memory, and your card has Micron memory, you may end up with a non-functional card. This problem can be resolved through blind flashing, but it can be time-consuming.

-Another issue is the display outputs. VBIOSes are configured based on the display output on the card. If you download a BIOS that is labeled as up-to-date but has a different display output scheme, some or none of the ports on your card may work in the best-case scenario. In the worst-case scenario, you may have to deal with blind flashing again.

-Updating the graphics card BIOS doesn't add much value. Manufacturers rarely release VBIOS updates, and when they do, it is usually for problem-solving rather than improvement. For instance, a new VBIOS cannot add DirectX 12 support to your card.

-I recommend having an up-to-date BIOS and operating system in every message, but when it comes to the graphics card, I strongly advise against downloading and flashing a VBIOS from TPU unless it has been provided by the manufacturer. It is a risky procedure, and you may end up with a brick.

-The VBIOS in TPU is also prepared by the manufacturer, but if that specific VBIOS is not listed on your graphics card's support page, I do not recommend downloading and flashing it yourself.



## For AMD:
First, we find our graphics card model on the following website:

https://www.techpowerup.com/vgabios/

Once you find the model, look for the latest one based on the date. The sorting format is Year/Month/Day. Download the BIOS accordingly and save it on your desktop or any other easily accessible location.

We will use the ATIFlash program to perform the BIOS flashing for AMD. You can download the program from the following link:

https://www.techpowerup.com/download/ati-atiflash/

After downloading, extract it to a folder and run the "amdvbflashWin" application as an administrator.
First, click on the Save option to create a backup of your current BIOS in case any issues arise.
Click on the Load Image option and browse for your BIOS file. Then click on Program to write the BIOS. The process will start and finish quickly, and your display may flicker during this time. After writing the BIOS, make sure to restart your system.

Note: Do not interrupt the power supply to your computer until the process is completed. The user is solely responsible for any consequences.

## For Nvidia:

First, we find our graphics card model on the following website:
https://www.techpowerup.com/vgabios/

SS2: 
<img src="https://github.com/typewordgorkem/project_reborn/blob/main/ekran1.PNG" width="auto">


Once you find the model, look for the latest one based on the date. The sorting format is Year/Month/Day. If the dates are the same, download the latest one.



## We will do the BIOS installation process with the NVFlash program for Nvidia. You can download the program from the link below;
https://www.techpowerup.com/download/nvidia-nvflash/

## Vga_bios update steps:

IMPORTANT NOTE: There are some discussions on foreign forums stating that only the refresh model of the GPU will work for flashing to 115W. I haven't personally tested it, so I can't provide any guarantees, but there is a possibility!

First, to be prepared for any potential issues, let's download GPU-Z and save our current BIOS. To do this, click on the arrow marked in yellow in the image and select the location where you want to save the BIOS.

SS3: 

<img src="https://github.com/typewordgorkem/project_reborn/blob/main/ss%203.PNG" width="auto">


## Flash time!
Now we have reached the flashing phase! 🙂 First, extract the NVFlash program in the .exe format from the downloaded .RAR file directly into a folder named "nvflash" that you will create under Local Disk C. Also, place the downloaded .ROM file in the same folder. It should be like this:

SS4: 
<img src="https://github.com/typewordgorkem/project_reborn/blob/main/SS4.PNG" width="auto">

This step is not mandatory, but I use it for convenience.

Next, type CMD in the search bar at the bottom left and run it as administrator. Select the nvflash folder we created using the following commands:

cd/nvflash
Now we are inside the nvflash folder. Let's start by disabling protection.
nvflash --protectoff
Running this command should be sufficient. The final screen should look like this:

SS5: 
<img src="https://github.com/typewordgorkem/project_reborn/blob/main/SS5.PNG" width="auto">

Moreover,
nvflash -6 (name of the downloaded BIOS file).rom
For example, "nvflash -6 232273.rom"
Let's start flashing with this command. The program will ask if you are sure, press "y" and hit enter. It may ask you again to make sure, again reply with "y". I think on some PCs, you might be asked to type "YES" instead of "y". The program will guide you on what to enter.

Once the process is complete, you will see two messages: "Firmware image has been updated..." and "a reboot is required...". Or you might see a message indicating success. It will inform you if the process was successful or not, so don't worry. Unfortunately, I don't have a visual for this final step.

Restart the system and enjoy the new BIOS. If you encounter any issues, follow the same steps and try flashing back the original BIOS that we backed up initially. If there are issues with the RTX 2060, you can try getting display output through Intel HD Graphics.

## Stay Tuned for part 2 : throttlestop tutorial!
#typewordgorkem
