A SBC based on the Signetics 2650 CPU. 

Specs:
- Running at 1 MHz clock speed
- Has 2K EPROM (0x000..0x7FF) which contains: 
    - PIPBUG v2: (0x000..0x3FF) a basic monitor program
      - can view/change memory content
      - can view/change regiser content
      - can load/save to papertape
      - etc. 
    - PIPLA: (0x400..0x7FF) a basic line assembler 
      - allows to enter mnemonics 
      - has basic pseudo-mnemonics (ORG, LBL, ASCI, ...) 
- Has 256 bytes RAM (0x800..0x8FF) 
  - 0x800..0x83F : reserved for PIPBUG and PIPLA
  - 0x840..0x8FF : available for user
- Uses SENSE and FLAG pins for serial comms at 110 or 300 baud
- After power-on and reset, user should type 'U' which will auto-select baudrate 
