

Telegram Channel Statistic Generator
===

Simple Python script to dump Telegram logs and generate html/png statistics.

Dependencies
---
* Python3
* Telegram-cli https://github.com/vysheng/tg/
* Matplotlib http://matplotlib.org/
* pytg https://github.com/luckydonald/pytg/



Getting started
---

1) Download and compile telegram-cli. Use the test branch!
```

./configure
make
```

2) Start the client with JSON support
```
```

3) Dump dialogs to find correct id for the channel. Copy the id!
```
$ ./dump.py --dialogs
```

4) Start dumping messages.

If the dump script is terminated it stores it's current offset to "name_offset"
file and the script tries always to continue from the last position.
Remove the offset file when you need to start from the beginning or use 

Note: When executed the first time initdb is required.

```
$ ./dump.py --initdb --id <your id> --name test
```

5) To update
```
$ ./dump.py --id <your id> --name test
```

6) Generate stats
```
$ ./generate.py test
```

7) View stats at "test" folder