# ToddlerJukeBox
Toddlers can be their own DJ with RFID cards

## What is it?
This is a Node-RED flow which reads the ID number from a NFC card and play the corresponding folder link with VLC media player.

## Why?
I want my toddler turn on his music without any help.

## How does it work?
Node-RED gets the ID number from the card reader. This input is first prepared (filtered) for the later comparison. The flow uses a text file as a database. The file link has to be set in the node "get textfile". The IDs and the corresponding links have to be separated by semicolons.
The file has to look like follows:
```
<ID>;<LINK>;
<ID>;stop;      // to stop the play list
<ID>;shutdowm;  // turn off the computer if Node-RED runs as sudo
```

## How to get the ID?
The card reader is recognized as a keyboard from the operating system. You just have to open an editor and put the card on the reader. You will see immediately the ID number.
