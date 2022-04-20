# Indala40134reverse
my attempt  to reverse engineer the Indala 40134
now it works only with  219 faculty code, card number is only From 0 to 16383 and crc isn't working properly yet 
Indala 40134 is 40 bit format - 40 bits are:
|1   |CN2  |CN15?|CN15?|crc+|crc-|FC?  |CN15?|CN1       |CN8        |
|CN11|CN15?|CN4  |CN15?|CN3 |FC? |CN15?|CN13|FC5?orCN14?|FC5?orCN14?|
|CN7 |FC?  |FC?  |FC6? |pH  |CN9 |CN10 |CN5 |pL         |FC?        |
|CN12|CN0  |CN15?|CN15?|CN15?|CN15?|CN15?|CN15?|FC?     |CN6        |
cn0-cn15 are bits of card number, fc0-fc7 are bits of faculty code, crc is a checksum ( crc+|crc- = 1|0 or 0|1 ), pH is even parity of fc0-fc7 and cn12-cn15, 
pL is odd parity of cn0-cn11. i'm not shure about certan bits, so they are marked with "?"
