# Receipt.js Designer

A development tool to edit, preview, and print the receipt markdown.  
https://receiptline.github.io/receiptjs-designer/  

![designer](ogp/en.png)  

```
^^^RECEIPT

03/18/2024, 12:34:56 PM
Asparagus | 1| 1.00
Broccoli  | 2| 2.00
Carrot    | 3| 3.00
---
^TOTAL | ^6.00
```

![example](resource/example.png)  


# Web browsers

- Modern Web browsers

The print function is available on Chrome, Edge, and Opera for PCs that support the Web Serial API.  
(Windows, Linux, Mac, and ChromeOS)  


# Receipt Printers

- Epson TM series
- Seiko Instruments RP series
- Star MC series
- Citizen CT series
- Fujitsu FP series

Connect with the Web Serial API.  
(Bluetooth, virtual serial port, and serial port)  

Epson TM series (South Asia model) and Star MC series (StarPRNT model) can print with device font of Thai characters.  

## Restrictions

### When connecting a USB printer with Epson TM Virtual Port on Windows

Closing the virtual port to which no printer is connected may cause the browser to stop responding.  
Please change the signal line setting to "RS-232C cross cable".  

![tmvpd](resource/tmvpd.png)  

If the printer goes offline during print data transmission and the virtual port is closed, the browser may stop responding.  
In this case, press the printer's paper feed button.  


# License

- Receipt.js
  - Apache License, Version 2.0
- QR Code Generator for JavaScript with UTF8 Support
  - MIT License
