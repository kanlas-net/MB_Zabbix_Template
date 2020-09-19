# Mount&Blade Dedicated Server Zabbix Template
Collects general server statistics and maps/players monthly statistics. If you don't need to collect player or/and map statistics just disable appropriate discovery rules.

To parse logs write right path to `{$LOG_PATH}` macros. Also change `{$PORT}` macros if server uses another port. `{$MELEE}` and `{$RANGED}` macros are used for melee/ranged players kills calculations, they depends on weapon icons names in log files.

:warning: **Be aware that first parsing of server logs to collect players stats will cost huge amount of resources. To prevent this just delete or move old logs.**
