# HITCON 2024 PCB Badge BadUSB Guide
BadUSB 使用說明/ BadUSB Guide

## 目錄/ TOC

1. [BadUSB 腳本燒錄方式/ How to put your BadUSB script into badge](#badusb-腳本燒錄方式-how-to-put-your-badusb-script-into-badge)  
2. [BadUSB 檔案格式/ BadUSB File Format](#badusb-檔案格式-badusb-file-format)  
3. [指令語法/ Command Set](#command-set)  
   3.1 [Comment Line](#comment-line)  
   3.2 [Delay](#delay)  
   3.3 [Special Keys](#special-keys)  
   3.4 [Modifier Keys](#modifier-keys)  
   3.5 [String](#string)  
   3.6 [String Delay](#string-delay)  
   3.7 [Repeat](#repeat)  
   3.8 [語法資料參考/ Reference](#語法資料參考-reference)  

## BadUSB 腳本燒錄方式/ How to put your BadUSB script into badge

可以透過 BadgeCommander 程式設定 BadUSB 腳本：[下載連結](https://github.com/john0312/hitcon-pcb-badge/releases/)
如果需要幫忙可前往活動組服務台詢問。  
You can put your BadUSB script into your badge with the BadgeCommander program: [Download Link](https://github.com/john0312/hitcon-pcb-badge/releases/)
If you need any support, please reach out to the Events Support Desk for help.  

## BadUSB 檔案格式/ BadUSB File Format

HITCON PCB Badge BadUSB 大致上與 USB Rubber Ducky 1.0 and Flipper 腳本語言相容，以下是你可使用的指令與語法:  
HITCON PCB Badge BadUSB is mostly compatible with USB Rubber Ducky 1.0 and Flipper Scripting Language, the following is the syntax you can use:  


## Command set

### Comment line
Just a single comment line. The interpreter will ignore all text after the REM command.

| Command | Parameters    | Notes |
|---------|---------------|-------|
| REM     | Comment text   |       |

### Delay
Pause script execution by a defined time.
Note: Delay Cannot be greater than 2500 ms.


| Command        | Parameters         | Notes                          |
|----------------|--------------------|--------------------------------|
| DELAY          | Delay value in ms  | Single delay                   |
| DEFAULT_DELAY  | Delay value in ms  | Add delay before every next command |
| DEFAULTDELAY   | Delay value in ms  | Same as DEFAULT_DELAY          |

### Special keys

| Command         | Notes             |
|-----------------|-------------------|
| DOWNARROW / DOWN|                   |
| LEFTARROW / LEFT|                   |
| RIGHTARROW / RIGHT|                 |
| UPARROW / UP    |                   |
| ENTER           |                   |
| DELETE          |                   |
| BACKSPACE       |                   |
| END             |                   |
| HOME            |                   |
| ESCAPE / ESC    |                   |
| INSERT          |                   |
| PAGEUP          |                   |
| PAGEDOWN        |                   |
| CAPSLOCK        |                   |
| NUMLOCK         |                   |
| SCROLLLOCK      |                   |
| PRINTSCREEN     |                   |
| BREAK           | Pause/Break key   |
| PAUSE           | Pause/Break key   |
| SPACE           |                   |
| TAB             |                   |
| MENU            | Context menu key  |
| APP             | Same as MENU      |
| Fx              | F1-F12 keys       |

### Modifier keys
Can be combined with a special key command or a single character.

| Command        | Notes              |
|----------------|--------------------|
| CONTROL / CTRL |                    |
| SHIFT          |                    |
| ALT            |                    |
| WINDOWS / GUI  |                    |
| CTRL-ALT       | CTRL+ALT           |
| CTRL-SHIFT     | CTRL+SHIFT         |
| ALT-SHIFT      | ALT+SHIFT          |
| ALT-GUI        | ALT+WIN            |
| GUI-SHIFT      | WIN+SHIFT          |
| GUI-CTRL       | WIN+CTRL           |

### String

| Command  | Parameters  | Notes                  |
|----------|-------------|------------------------|
| STRING   | Text string | Print text string       |
| STRINGLN | Text string | Print text string and press enter after it |

### String delay
Delay between keypresses.

| Command            | Parameters         | Notes                                      |
|--------------------|--------------------|--------------------------------------------|
| STRING_DELAY       | Delay value in ms  | Applied once to next appearing STRING command |
| STRINGDELAY        | Delay value in ms  | Same as STRING_DELAY                       |
| DEFAULT_STRING_DELAY | Delay value in ms  | Apply to every appearing STRING command     |
| DEFAULTSTRINGDELAY | Delay value in ms  | Same as DEFAULT_STRING_DELAY               |

### Repeat

| Command | Parameters               | Notes                      |
|---------|--------------------------|----------------------------|
| REPEAT  | Number of additional repeats | Repeat previous command     |

### 語法資料參考/ Reference
此語法說明文件是參考 [Flipper Zero Firmware: BadUSB File Format](https://developer.flipper.net/flipperzero/doxygen/badusb_file_format.html) 製成。  
This documentation is based on [Flipper Zero Firmware: BadUSB File Format](https://developer.flipper.net/flipperzero/doxygen/badusb_file_format.html).  
