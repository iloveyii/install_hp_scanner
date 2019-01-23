Install HP Printer utilities on Ubuntu
=====================================

This repo has instructions on how to install the required packages/plugins on Ubuntu to be able to scan from Ubuntu command line.





## Installations

  * Clone the repository: `git clone https://github.com/iloveyii/install_hp_scanner`.
  * Find the URI to the network printer: `scanimage -L `  and adjust this in the script.
  * Make the script executable `sudo chmod 777 scan_image_to_png`.
  * Move it to bin `sudo mv scan_image_to_png /usr/local/bin/`.
  
  
### Usage
  
  * To scan the document in color mode use : `scan_image_to_png fileName.png color`
  * To scan the document in black and white mode use : `scan_image_to_png fileName.png`
  
  It will save the scanned image in the current directory.
  
### Requirements

   * You many need to install the following.
   
`
   sudo apt-get install hplip
   sudo apt install snmp
   sudo apt-get install hplip-gui
   sudo chmod 777 hplip-3.18.12-plugin.run
   ./hplip-3.18.12-plugin.run
   sudo hp-setup
   hp-plugin
`