# Windows Server 2019 Evaluation copy and Windows 10 Client - How to extend trial 

1) Windows Server 2019 -> Control  Panel, change date to 2-3 months earlier. run -> gpupdate. CMD as admin:

```
slmgr -rearm
```
Restart.

2) Windows 10 Client. Sync date with domain controller as admin:

```
w32tm /config /syncfromflags:domhier /update

net stop w32time && net start w32time
```
Restart.
