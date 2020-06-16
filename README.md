# Hackintosh macOs Catalina on a Dell Inspiron 5570
This is a post-install guide for macOs Catalina on a hackintosh pc, so i am assuming that you've successfully installed macOs Catalina on your machine. 
If not, you can download Catalina iso image from [OLARILA website](https://www.olarila.com/topic/6278-new-olarila-images/) and download [balenaEtcher](https://www.balena.io/etcher/) to create a bootable usb drive to be able to install Catalina. (there are a lot of tutorials and guides that shows how to install it and it's pretty easy, so please go ahead and google it) 

I would like to give credits to : 

a) The website www.tonymacx86.com 

b) Jack Zhang's EFI folder for Mojave [click here](https://www.youtube.com/watch?v=PZ5cgrZ_jX0&t=1s) to check it out

c) Floricello for EFI updates and modifications for compatibility with Catalina [click here](https://www.tonymacx86.com/threads/success-with-dell-inspiron-5570-macos-catalina-installation-with-and-without-the-dangerous-bios-editing.298391/) to check it out


Laptop specifications :
- CPU : Intel(R) Core(TM) i7-8550U CPU @ 1.80GHz
- RAM : 8GB DDR4 2400 Mhz
- SSD : samsung ssd 850 evo 250 go 
- GPU : Intel UHD Graphics 620


What is working : 
- Graphics acceleration
- audio/ microphone/ audio control (F2 & F3)
- trackpad
- display brightness/ brightness control (F11 & F12)
- battery managment

Note : sound on headphones is also working, please follow 'Headphones sound fix' down below. 


What is not working : 
- sleep/wake 
- wifi (you can still purchase a macOs compatible wifi card such as DW1707, DW1820A or DW1560A)

Note : I have made a video on how to install DW1820A since it's the one i'm using --> please [click here](https://www.youtube.com/watch?v=KttwKmIwOBU&t=20s) to check it out.


What you need : 
- [Clover Configurator](https://www.macupdate.com/app/mac/61090/clover-configurator) 
- [Kext Utility](https://www.hackintoshzone.com/files/file/537-kext-utility-super-speed-edition/)


### EFI and clover configuration
Basically you just have to download the EFI folder by clicking on "clone or download", or you can open your terminal and type the following command :
``` git clone https://github.com/FERARMAO/Hackintosh-Catalina-Dell-5570.git ```
Then mount your EFI partition using clover configurator, open it, and put the EFI folder there. (replace if there is an existant EFI folder)
That's pretty much it, now restart your laptop.


### Headphones sound fix
Go to EFI/clover/kexts/other and copy codeccommander.kext and paste it in /Library/Extensions, then run kext utility, type your password, and don't close it until it's done setting up proper permissions.
Restart your pc, headphones sound should be fixed. 


### !Important! : 
I haven't done any BIOS editing so it's by default.
You can edit your BIOS by following [this guide](https://www.tonymacx86.com/threads/success-with-dell-inspiron-5570-macos-catalina-installation-with-and-without-the-dangerous-bios-editing.298391/) but **DO IT AT YOUR OWN RISK !** I am not responsible of any damages you can have on your laptop.














