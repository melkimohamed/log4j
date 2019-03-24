# log4j
--------DailyRollingFileAppender
1- DailyRollingFileAppender  not support compression
2- DailyRollingFileAppender does not have a maxBVackupIndexp roperty



--------------RollingFileAppender
RollingFileAppender support MAX_HISTORY
https://community.hortonworks.com/articles/50058/using-log4j-extras-how-to-rotate-as-well-as-zip-th.html

RollinFileAppender  avec TimeBasedRollingPolicy
-Accept la compression et Maxhistory

log4j.rootLogger=INFO,
loggerId log4j.appender.loggerId=org.apache.log4j.rolling.RollingFileAppender 
log4j.appender.loggerId.rollingPolicy.MaxHistory=5 
log4j.appender.loggerId.triggeringPolicy=org.apache.log4j.rolling.TimeBasedTriggeringPolicy log4j.appender.loggerId.triggeringPolicy.MaxFileSize=10000000
log4j.appender.loggerId.rollingPolicy.FileNamePattern=hive.%d.gz
log4j.appender.loggerId.rollingPolicy.ActiveFileName=hive.log
log4j.appender.loggerId.layout=org.apache.log4j.PatternLayout
log4j.appender.loggerId.layout.ConversionPattern=%d [%t] %-5p (%F:%L) - %m%n
