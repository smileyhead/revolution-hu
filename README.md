# Wii magyarítás – _Wii Hungarian Translation_
A Wii rendszeralkalmazásainak és beépített csatornáinak a magyarítása, WiiLinkes használathoz.

_Hungarian translations of Wii system software &amp; built-in channels for use with WiiLink._

## Jogi megjegyzés – _Legal Notice_
Ez a repó csak a módosított nyelvi fájlokat és a hozzájuk tartozó üres könyvtárstruktúrákat tartalmazza, biztonsági másolati és kézi módosítási szempontok miatt. A csatornák eredeti kódja, kellékei vagy egyéb tartalma itt nem található meg.

_This repo only contains the modified language files and their corresponsing empty file directory structures, as a backup and for manual patching. The channels' original code, assets, or other contents are not hosted here._

## Előkövetelmények – _Prerequisites_
1. [Wiimms SZS Tool](https://szs.wiimm.de/wszst/)
2. [Nintendo DS Compressors](https://github.com/PeterLemon/Nintendo_DS_Compressors)

## Módosítási utasítások – _Patching Instructions_
### Wii menü – Wii Menu
1. `cd \00000001\00000002\content\0000009a.d\message\eng`
2. `wbmgt encode ipl_common_noe.txt`
3. `cd \00000001\00000002\content`
4. `wszst create 0000009a.d`
5. 0000009a.u8 -> 0000009a.app

### Wii Room
1. `cd \00010001\4843494a\content\00000026.d\msg`
2. `wbmgt encode message.txt`
3. `lzss -evf message.bmg message.lex`
4. `cd \00010001\4843494a\content`
5. `wszst create 00000026.d`
6. 00000026.u8 -> 00000026.app

### Miiversenycsatorna – _Mii Contest Channel / Check Mii Out Channel_
1. `cd \00010001\48415050\content\0000000d.d\content4\Message\Bmg`
2. `wbmgt encode Basic_EN.txt`
3. Basic_EN.bmg -> Basic_EN.szs
4. `cd \00010001\48415050\content`
5. `wszst create 0000000d.d`
6. 0000000d.u8 -> 0000000d.app
