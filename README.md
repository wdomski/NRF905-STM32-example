# NRF905-STM32-example

Example for NRF905 radio module. 

This project is build for Nucleo64-L452RE dev board.

After cloning the repository all submodules have to be updated. 
This can be done with

```
git submodule update --init --recursive
```

# Sample output

Output from the master:

```
Mode: Master, TX, 25D34478
Reg conf: 0A, 0C, 44, 20, 20, 9B, C5, A0, 6D, D8, 
Sending (23): Hello 0, from 25D34478!
ret = 1
Switching to RX (25D34478)
Waiting for max 2500 ms
No response
Sending (23): Hello 1, from 25D34478!
ret = 1
Switching to RX (25D34478)
Waiting for max 2200 ms
Received: Hello 0, from 6DA0C59B!
Switching to TX (25D34478)
Sending (23): Hello 2, from 25D34478!
ret = 1
Switching to RX (25D34478)
Waiting for max 2800 ms
Received: Hello 1, from 6DA0C59B!
Switching to TX (25D34478)
Sending (23): Hello 3, from 25D34478!
ret = 1
Switching to RX (25D34478)
Waiting for max 2100 ms
No response
Sending (23): Hello 4, from 25D34478!
ret = 1
Switching to RX (25D34478)
Waiting for max 3900 ms
Received: Hello 3, from 6DA0C59B!
Switching to TX (25D34478)
Sending (23): Hello 5, from 25D34478!
ret = 1
Switching to RX (25D34478)
Waiting for max 2100 ms
No response
Sending (23): Hello 6, from 25D34478!
ret = 1
Switching to RX (25D34478)
Waiting for max 2600 ms
```

Output from the slave:

```
Mode: Slave, RX, 6DA0C59B
Reg conf: 0A, 0C, 44, 20, 20, 78, 44, D3, 25, D8, 
Sending (23): Hello 0, from 6DA0C59B!
ret = 1
Switching to RX (6DA0C59B)
Waiting for max 3700 ms
Received: Hello 2, from 25D34478!
Switching to TX (6DA0C59B)
Sending (23): Hello 1, from 6DA0C59B!
ret = 1
Switching to RX (6DA0C59B)
Waiting for max 3500 ms
Received: Hello 3, from 25D34478!
Switching to TX (6DA0C59B)
Sending (23): Hello 2, from 6DA0C59B!
ret = 1
Switching to RX (6DA0C59B)
Waiting for max 3800 ms
Received: Hello 4, from 25D34478!
Switching to TX (6DA0C59B)
Sending (23): Hello 3, from 6DA0C59B!
ret = 1
Switching to RX (6DA0C59B)
Waiting for max 3400 ms
Received: Hello 5, from 25D34478!
Switching to TX (6DA0C59B)
Sending (23): Hello 4, from 6DA0C59B!
ret = 1
Switching to RX (6DA0C59B)
Waiting for max 3600 ms
Received: Hello 6, from 25D34478!
Switching to TX (6DA0C59B)
```

As it can be seen master sends data to the slave. 
Then the slave sends the data to the master.
The process repeats itself in an endless loop.
