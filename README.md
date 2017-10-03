# tcpser-dummy
tcpser with dummy functionality
```
Usage: ./tcpser <parameters>
  -p   port to listen on (defaults to 6400)
  -t   trace flags: (can be combined)
    's' = modem input
    'S' = modem output
    'i' = IP input
    'I' = IP output
  -l   0 (NONE), 1 (FATAL) - 7 (DEBUG_X) (defaults to 0)
  -L   log file (defaults to stderr)

  The following can be repeated for each modem desired
  (-s, -S, and -i will apply to any subsequent device if not set again)

  -d   serial device (e.g. /dev/ttyS0). Cannot be used with -v
  -v   tcp port for VICE RS232 (e.g. 25232). Cannot be used with -d
  -s   serial port speed (defaults to 38400)
  -S   speed modem will report (defaults to -s value). Setting to 555 or speed*23 enables dummy mode
  -I   invert DCD pin
  -n   add phone entry (number=replacement)
  -a   filename to send to local side upon answer
  -A   filename to send to remote side upon answer
  -c   filename to send to local side upon connect
  -C   filename to send to remote side upon connect
  -N   filename to send when no answer
  -B   filename to send when modem(s) busy
  -T   filename to send upon inactivity timeout
  -i   modem init string (defaults to '', leave off 'at' prefix when specifying)
  -D   direct connection (follow with hostname:port for caller, : for receiver)
  -S 555 dummy mode, exits after sending CONNECT, useful for connecting Windows to serial internet
  -S speed*23 dummy mode, exits after sending CONNECT SPEED, useful for connecting Windows to serial internet
```
