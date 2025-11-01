# Receipt.js Designer

A development tool to edit, preview, and print the receipt markdown.  
https://receiptline.github.io/receiptjs-designer/  

![designer](ogp/en.png)  


# Editor and viewer

Main area for editing a receipt markdown file.  
This preview is displayed side by side.  

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


# Menu bar

## File

|Control|Description|
|---|---|
|![open](resource/open.png)|Open receipt markdown (\*.receipt, \*.txt)|
|![download](resource/download.png)|Download receipt markdown (\*.receipt), plain text (\*.txt), SVG image (\*.svg), or PNG image (\*.png)|
|![print](resource/print.png)|Print receipt markdown|
|![option](resource/option.png)|Set print options|

## Insert

|Control|Description|
|---|---|
|![image](resource/image.png)|Insert image<br>`{image:...}`|
|![barcode](resource/barcode.png)|Insert barcode<br>`{code:...; option:...}`|
|![2dcode](resource/2dcode.png)|Insert 2D code<br>`{code:...; option:...}`|
|![format](resource/format.png)|Insert formatting<br>`{width:...; border:...; text:...; align:...}`|

## Edit

|Control|Description|
|---|---|
|![column](resource/column.png)|Add Column delimiter<br> <code>&#x7c;</code>|
|![hr](resource/hr.png)|Add horizontal rule<br>`-`|
|![cut](resource/cut.png)|Add paper cut<br>`=`|
|![ul](resource/ul.png)|Underline text<br>`_`|
|![em](resource/em.png)|Emphasize text<br>`"`|
|![invert](resource/invert.png)|Invert text<br>`` ` ``|
|![size](resource/size.png)|Enlarge text<br>`^`|

## View

|Control|Description|
|---|---|
|![zoom](resource/zoom.png)|Zoom in/out|
|![language](resource/language.png)|Select language|
|![width](resource/width.png)|Change print width (cpl: characters per line)|
|![landscape](resource/landscape.png)|Enable/Disable landscape orientation|
|![spacing](resource/spacing.png)|Enable/Disable line spacing|


# Web browsers

The print function is available on Chrome, Edge, and Opera that support the Web Serial API.  
(Windows, Linux, macOS, ChromeOS, and **Android**)  


# Receipt printers

- Epson TM series
- Seiko Instruments RP series
- Star MC series
- Citizen CT series
- Fujitsu FP series

Connect with the Web Serial API.  
(Bluetooth, virtual serial port, and serial port)  

Epson TM series (South Asia model) and Star MC series (StarPRNT model) can print with device font of Thai characters.  

## Restrictions

The Web Serial API has no write timeout, so if hardware flow control is enabled, opening the printer cover during printing may cause the browser to stop responding. In this case, close the printer cover or press the paper feed button. Alternatively, change the printer's busy condition setting from "Offline or receive buffer full" to "Receive buffer full".  

_The restriction on Epson TM Virtual Port on Windows that existed in previous versions has been resolved. There is no need to change the signal line settings._  
