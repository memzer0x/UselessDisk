# UselessDisk
I had some time to waste and found this really simple piece of malware called **UselessDisk** on [app.any.run](https://app.any.run), i decided i was going to reprogram it since it was pretty small.

The program just open a handle on `\\\\.\\PhysicalDrive0` which contains Windows Master Boot Record, it then overwrite the content of the Master Boot Record and force the system to reboot.

You have to note that program which interacts with the MBR are usually always detected by antiviruses, putting this code snippet in a malware would just make it a LOT harder to obfuscate. 

I upload the code strictly for educational purposes and i take no responsibility to anything you do with the code...

One other thing to note, is that you can change the payload `Yeeeted variable in the source code`, for something else, this will allow you to choose the text that appears on the screen when the computers tried to boot inside the overwritten MBR, to simplify your life i made [MBR-PaYz](https://github.com/memzer0x/MBR-PaYz) which you can use for generating MBR payloads.

<p align="center">
  <img src="https://cdn.discordapp.com/attachments/895523353316716605/921402395769077760/unknown.png"/>
</p>
