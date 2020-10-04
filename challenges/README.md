# ESC'20 Challenge Releases

This folder contains all available challenge sets released so far.
Each set contains independent challenges to solve and all points from all challenges are accumulated in the final score of each team. Challenges are given a different number of points based upon their difficulty;
the number of points for each challenge is revealed once the challenge is solved.

## Uploading hex files to the board

First install [SiFive Freedom E SDK]([https://github.com/sifive/freedom-e-sdk#setting-up-the-sdk](https://github.com/sifive/freedom-e-sdk#setting-up-the-sdk)) and ensure that all prerequisites are also installed.

Plug your board into a USB port on your system and then from the top-level directory of the Freedom E SDK, enter the following command in your terminal:

```
scripts/upload --hex <REPLACE_WITH_PATH_TO_HEX_FILE>/<NAME_OF_HEX_FILE>.hex --jlink <REPLACE_WITH_PATH_TO_JLINKEXE>/JLinkExe
```

Make sure to restart your board (press the red button) after the **hex** file is successfully uploaded. Note: the .elf files should not be uploaded to the board.  

## Communicating with the RISC-V Processor

When the board is successfully programmed with a challenge .hex file, it will automatically create a WiFi network called “ESC-2020”. When the blue LED stops blinking and becomes steady, the board is ready to accept connections. In case the LED does not turn steady blue after a few seconds, reset the board and turn your WiFi off and then on again.

To connect to the board over WiFi from your computer and be able to send and receive data over TCP, you can use the following command:

```
nc 192.168.4.7 50200
```

After a connection is successfully established, the green LED of the board will turn on. You will be greeted with welcome messages from the board and it will prompt you with further instructions, if necessary. If you enter an incorrect solution to the challenge, you will receive a 'Challenge Failed' or 'Incorrect' message over netcat. To try again, restart the board, kill the current netcat connection on your computer and initialize a new one after the blue LED stops blinking. You may also have to reconnect over WiFi. If you enter a correct solution, you will receive a congratulatory message over netcat.
