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
