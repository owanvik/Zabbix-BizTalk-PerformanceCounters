# Zabbix-BizTalk-PerformanceCounters
BizTalk Performance Counters template for Zabbix

This template discovers all performance counters for BizTalk and creates items and triggers for them using LLD.

Some of the macros are "User macro with context" which you can read about here:
https://www.zabbix.com/documentation/current/en/manual/config/macros/user_macros_context

Example: {$ACTIVE.INSTANCE.COUNT.CRIT:"MyBT.HostInstance"}
This will override the default {$ACTIVE.INSTANCE.COUNT.CRIT} macro for "MyBT.HostInstance".
To use this you create a new macro like {$ACTIVE.INSTANCE.COUNT.CRIT:"MyBT.HostInstance"} and replace "MyBT.HostInstance" with the host name of your host instance.

Known issues:
- Performance counters sometimes report no data, giving you blank spots in graphs
- Message counts have no purpose in this template


