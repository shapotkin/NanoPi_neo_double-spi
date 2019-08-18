# NanoPi_neo_double-spi
Some scripts to activate both SPI busses of Allwinner sun8i-h3 in Armbian
<p>Scripts was creapted and checked for <a href="http://nanopi.io/nanopi-neo-core.html">NanoPi Neo Core</a> board</p>
<p>Revised scripts could be used for other SOC's</p>
<p>Scripts must be running with root's rights, so you HAVE to be sure what are you doing</p>
<p>This steps was created according <a href="https://forum.armbian.com/topic/10381-nanopi-neo-core-how-to-activate-a-second-spi/?tab=comments#comment-80893">Armbian forum disscussion</a> </p>

<ul>
<li>Step 1: Decompilation of the main .dtb file and backup of it.
<li>Step 2: In any text editor remove all uart3*{} sections and uart3* paramenters. The script is just a help message.
<li>Step 3: Compile a new .dtb file.
<li>Step 4: Compile a new overlay-user .dtbo file with both SPIs support
<li>Step 5: In any text editor remove all references to spi from /boot/armbianEnv.txt, reboot and enjoy with double SPI on your system
</ul>
<p>After that the UART3 will be unavalable. So you have to select what is important for you: 2xSPI or UART3.
That limitation because of pins conflict. 
Please refer to https://docs.armbian.com/User-Guide_Allwinner_overlays/ <b>Overlay pinmux conflicts</b></p>

Regards