# Mount&Blade Dedicated Server Zabbix Templates
### Templates created for zabbix 5.x, I didn't test them on older versions.
Collects general server statistics and maps/players monthly statistics. 
If you don't need to collect  map statistics just disable appropriate discovery rule.
To collect players statistics link players stats template.

Change `{$PORT}` macros if server uses another port.
Players stats template needs to parse logs, so you should write right path to `{$LOG_PATH}` macros at host. `{$MELEE}`, `{$RANGED}` and `{$HEADSHOT}` macros are used for melee/ranged players kills calculations, they depends on weapon icons names in log files.

:exclamation: **You should set `EnableRemoteCommands=1` or `AllowKey=system.run[*]` in zabbix agent configuration**

:exclamation: **If you encountered timeout issues with active checks items set `Timeout` value greater than 3 (3 is default) in zabbix agent configuration**

:exclamation: **For player stats template you may need to increase zabbix server `ValueCacheSize` parameter if you use default one.**

:warning: **Be aware that first parsing of server logs for player stats template will cost huge amount of resources. To prevent this just delete or move old logs.**
