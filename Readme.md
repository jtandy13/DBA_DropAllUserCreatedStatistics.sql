# DBA_DropAllUserCreatedStatistics.sql

User created statistics are easy to identify from the sys.statistics. Just use the user_created column; it's either a 1 or a zero. From there we are just gathering the schema name, object name, and statistics name in oder to create the dynamic sql string. Once assembled, it is executed.

The loop teminates once the sql string has a Null value.