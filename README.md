# rfid32
Lua (NodeMCU) library for interfacing ESP32 with MFRC522 rfid card reader

## Usage

This example will print UID (in hexadecimal representation) of scanned rfid tag.

```lua
  require('rfid32')({
        pin_sda  = 22,
        pin_clk  = 19,
        pin_miso = 25,
        pin_mosi = 23
    })
    .init()
    .scan({
        got_tag = function(tag, rfid)
            print( tag.hex() )
        end
    })
```

## Dependencies

  The library depends on the following NodeMCU modules:
  - `spi`
  - `bit`
  - `tmr`
