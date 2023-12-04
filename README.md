# Minion Blast Tags
### NFC tag dumps for Universal Orlando Villain-Con Minion Blast collectibles

In Minion Blast, when using the app, there are 10 collectibles that can only be obtained by finding NFC pads in and around the attraction.
According to NFC Tools, these NFC pads announce themselves as NTAG215s, and contain 3 blocks of binary data followed by 10 blocks of text data.
The binary data and most of the text data appears to be the same across each tag, the only differences being in the final two blocks.
The text data is (I think) UTF-16 encoded, and reads `actionLootLocationXX`, where XX is a two digit number identifying the loot location.

The numbers follow the layout of the collectibles in the app, with 08 and 11 skipped. So, the IDs are:
01. Villain Network Channel Mug
02. Binky Nelson's Pacifier
03. Gru's Vicious 6 Underwear
04. Gru's Moon Heist Plans
05. Space Killer Ship
06. Pop-A-Nana
07. Minion Cupcake
08. *(unused)*
09. Papagena
10. Stuart's Ukelele (misspelled in the app)
11. *(unused)*
12. Gru's Wig

You'll have to imagine the zero-padding to two digits since it doesn't display in Markdown.

The files provided here are Proxmark3 dump files, with a `.json` and `.bin` for each.
Only blocks 0x04 to 0x10 (4 to 16) are important here, but the remaining zero bytes out to the size of NTAG215 are included since the dumps were produced from those.

This information is current as of 2023-12-04
