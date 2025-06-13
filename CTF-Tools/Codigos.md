# Fragmentos de código

```rust
use modbus::{Client, Coil};
use modbus::tcp;

let mut cfg = tcp::Config::default();
let mut client = tcp::Transport::new_with_cfg("127.0.0.1", cfg).unwrap();
assert!(client.write_single_coil(0, Coil::On).is_ok());
```

```python
from pymodbus.client.sync import ModbusSlave

slave = ModbusSlave(address=1, port="/dev/ttyUSB0", timeout=1)

registers = slave.read_holding_registers(start_address=0, quantity=10)

for register in registers:
    print(register)
```
