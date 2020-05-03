# ts-empty

Lists unused TeamSpeak channels and time of emptiness

The script will prompt you for connection details or you can specify them in environment variables

Example driver script:

```
#!/bin/sh

export TS_SERVERADMIN_USERNAME="serveradmin"
export TS_SERVERADMIN_PASSWORD="XXXXXX"
export TS_SERVER_ADDRESS="127.0.0.1"
export TS_SERVER_QUERY_PORT="10011"

./ts-empty
```

You can also ignore channels specified in `TS_IGNORED_CHANNELS`:

```
export TS_IGNORED_CHANNELS="
Channel 1
Channel 2
Channel 3
"
```

Example output:

```
322    |  Channel name 1   |  40 d, 23 hr, 29 min, 40 sec
12082  |  Channel name 2   |  24 d, 51 min, 24 sec
10667  |  Channel name 3   |  13 d, 3 hr, 10 min, 56 sec
9245   |  Channel name 4   |  10 d, 21 hr, 32 min, 7 sec
8385   |  Channel name 4   |  10 d, 11 hr, 39 min, 3 sec
9802   |  Channel name 5   |  8 d, 1 hr, 3 min, 41 sec
10060  |  Channel name 6   |  5 d, 2 hr, 32 min, 46 sec
9880   |  Channel name 7   |  4 d, 23 hr, 31 min, 9 sec
9750   |  Channel name 8   |  2 d, 22 hr, 8 min, 57 sec
11916  |  Channel name 9   |  2 d, 9 hr, 26 min, 21 sec
7186   |  Channel name 10  |  1 d, 23 hr, 49 min, 57 sec
9833   |  Channel name 11  |  1 d, 13 hr, 30 min, 14 sec
11553  |  Channel name 12  |  1 d, 56 min, 12 sec
11258  |  Channel name 13  |  1 d, 56 min, 11 sec
7115   |  Channel name 14  |  20 hr, 38 sec
11872  |  Channel name 15  |  5 hr, 7 min, 47 sec
12198  |  Channel name 16  |  3 hr, 35 min, 57 sec
9749   |  Channel name 17  |  1 hr, 40 min, 43 sec
11875  |  Channel name 18  |  1 hr, 29 min, 27 sec
11360  |  Channel name 19  |  1 hr, 27 min, 28 sec
```

*columns: CID | Channel name | time without use
