# Tools Used

# Gobuster

Used to brute force websites to find directories and subdomains that might be hidden

`gobuster -e -u {link} -w {wordlist path}`

^ for ex: gobuster -e -u [http://192.168.0.155/](http://192.168.0.155/) -w /usr/share/wordlists/dirb/common.txt

# Pdfinfo

Used to display pdf metadata, can be installed via: “`sudo apt install poppler-utils`”

`pdfinfo {Document}.pdf`

# Photo EXIF

Exchangeable Image File Format (EXIF) stores photo metadata, which often includes location. You can install a tool to read a photo’s EXIF via “`sudo apt install libimage-exiftool-perl`”

`exiftool {Image}.jpg`