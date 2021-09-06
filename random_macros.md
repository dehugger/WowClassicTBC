# Random Useful Macros

### Print tab delimited character loadout

```lua
/script local h,m=GetGameTime()a=GetUnitName('player')..'@'..h..'-'..m..'\n'..'Slot\tId\tName\n'd,n=''for s=0,19 do d=GetInventoryItemID("player",s)if(d)then n,z=GetItemInfo(d)a=a..tostring(s).."\t"..tostring(d).."\t"..n.."\n"end end print(a)
```

Outputs your characters name and the current server time (name@hh-mm), then your equipped items in tab delimited format with item slot, item id, and item name. 
If nothing is equipped in a slot then it will be skipped. This can be pasted directly into a spread sheet.
You can replace `print(a)` with `error(a)` to output the message to an error frame, which may be easier to copy text from if you do not have a chat addon like Prat.

Example output:
```
 Coffeeofdoom@21-36
Slot	Id	Name
1	29044	Netherblade Facemask
2	35507	Amulet of Bitter Hatred
3	28755	Bladed Shoulderpads of the Merciless
4	4333	Dark Silk Shirt
5	28601	Chestguard of the Conniver
6	28750	Girdle of Treachery
7	29046	Netherblade Breeches
8	25686	Fel Leather Boots
9	29246	Nightfall Wristguards
10	28684	Grand Marshal's Leather Gloves
11	22961	Band of Reanimation
12	30834	Shapeshifter's Signet
13	29383	Bloodlust Brooch
14	28034	Hourglass of the Unraveller
15	28672	Drape of the Dark Reavers
16	28524	Emerald Ripper
17	29346	Feltooth Eviscerator
18	28659	Xavian Stiletto
19	28788	Tabard of the Protector
```

The inventory slots are named thusly:
| SlotID | Name |
:--|-------:
0 | ammo
1 | head
2 | neck
3 | shoulder
4 | shirt
5 | chest
6 | waist
7 | legs
8 | feet
9 | wrist
10 | hands
11 | finger 1
12 | finger 2
13 | trinket 1
14 | trinket 2
15 | back
16 | main hand
17 | off hand
18 | ranged
19 | tabard
