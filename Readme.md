# DBA_DropAllUserCreatedStatistics.sql

User created statistics are easy enough to identify from the sys.stats system view on any database. Just use the user_created column; it's either a 1 or a zero. From there we are just gathering the schema name, object name, and statistics name in order to create the dynamic sql string. Once assembled, we can execute the drop.

The loop teminates once there are no more user created statistics.
