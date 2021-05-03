Install HP Printer utilities on Ubuntu
=====================================

This repo has instructions on how to install the required packages/plugins on Ubuntu to be able to scan from Ubuntu command line.

![Image](https://asset.conrad.com/media10/isa/160267/c1/-/sv/1500104_ZB_04_FB/image.jpg)

![Screenshot](https://raw.githubusercontent.com/iloveyii/install_hp_scanner/master/screenshot.png)



### Installations

  * Clone the repository: `git clone https://github.com/iloveyii/install_hp_scanner`.
  * Find the URI to the network printer: `scanimage -L `  and adjust this in the script. Try to print a document and the result may change but actually works!!!
  * Make the script executable `sudo chmod 777 scan_image_to_png`.
  * Move it to bin `sudo mv scan_image_to_png /usr/local/bin/`.
  
  
### Usage
  
  * To scan the document in color mode use : `scan_image_to_png fileName.png color`
  * To scan the document in black and white mode use : `scan_image_to_png fileName.png`
  * You may want to convert all images to pdf : `convert *.png all.pdf`
  * If trouble of permissions in the above command use: `sudo mv /etc/ImageMagick-6/policy.xml /etc/ImageMagick-6/policy.xmlout`
  
  It will save the scanned image in the current directory.
  
### Requirements

   * You many need to install the following.
   
```
   sudo apt-get install hplip
   sudo apt install snmp
   sudo apt-get install hplip-gui
   sudo chmod 777 hplip-3.18.12-plugin.run
   ./hplip-3.18.12-plugin.run
   sudo hp-setup
   hp-plugin
```


### Links
* [Convert error](https://stackoverflow.com/questions/42928765/convertnot-authorized-aaaa-error-constitute-c-readimage-453)
* [Download hp plugin latest](https://developers.hp.com/hp-linux-imaging-and-printing/plugins)
