# IMÁÄÌìÊÒ
Ò»¸ö»ùÓÚNettyµÄÁÄÌì¹¤¾ß£¨¿ª·¢ÖÐ£©£¬Ê¹ÓÃZookeeper+RedisÊµÏÖ·þÎñ¶Ë·Ö²¼Ê½²¿Êð¡£

## ÏµÍ³¼Ü¹¹
 ![image](https://github.com/xFive555/im/raw/master/pic/im.png)
-  `¿Í»§¶Ë`Óë`·þÎñ¶Ë`µÄÁ¬½Ó£¬Í¨¹ý`Â·ÓÉ¶Ë`Ñ¡Ôñ¿ÉÓÃ`·þÎñ¶Ë`½Úµã
-  `·þÎñ¶Ë`Æô¶¯ºó£¬Ïò`Zookeeper`×¢²á×Ô¼º
-  `¿Í»§¶Ë`·¢ËÍÏûÏ¢Í¨¹ý`Â·ÓÉ¶Ë`£¬Ñ¡Ôñ¶ÔÓ¦µÄ`·þÎñ¶Ë`½øÐÐÍÆËÍÏûÏ¢
-  `Â·ÓÉ¶Ë`ÎÞ×´Ì¬£¬¼¯Èº²¿ÊðÖ»ÐèÒªÒ»¸ö`Nginx`´úÀí¼´¿É
 
## TODO LIST
* [x] ¿Í»§¶Ë·þÎñ¶ËÁ¬½Ó
* [x] ¿Í»§¶Ë´¦ÀíÓÃ»§ÊäÈëÏûÏ¢
* [x] ÏûÏ¢ÐòÁÐ»¯£¨Protobuf£©
* [x] ·þÎñ¶Ë×¢²á
* [x] Â·ÓÉ¶Ë»ñÈ¡¿ÉÓÃ·þÎñ¶Ë½Úµã
* [x] ÏûÏ¢Èº·¢¹¦ÄÜ
* [x] ¿Í»§¶ËÏÂÏß£¨Ç¿ÖÆÏÂÏß/Ö÷¶¯ÏÂÏß£©
* [x] ·þÎñ¶Ë¶ÏÏß£¬¿Í»§¶ËÖØÁ¬
* [ ] ÐÄÌø
* [ ] ÏûÏ¢ÖØ·¢
* [ ] ÁÄÌì¼ÇÂ¼
* [ ] ÀëÏßÏûÏ¢

## ÔËÐÐ
1.Æô¶¯redisÓëZookeeper£¬ÐÞ¸Äredis¡¢ZookeeperÅäÖÃ

2.±àÒë¡¢´ò°ü
```
mvn -Dmaven.test.skip=true clean package
```
3.Æô¶¯Â·ÓÉ
```
java -jar im-route\target\im-route-0.0.1-SNAPSHOT.jar
```	
4.Æô¶¯·þÎñ¶Ë
```
java -jar im-server\target\im-server-0.0.1-SNAPSHOT.jar --server.port=8084 --im.server.port=8090
java -jar im-server\target\im-server-0.0.1-SNAPSHOT.jar --server.port=8085 --im.server.port=8091
```	
5.Æô¶¯¿Í»§¶Ë
```
java -jar im-client\target\im-client-0.0.1-SNAPSHOT.jar --server.port=8071 --im.user.id=1001 --im.user.userName=Five
java -jar im-client\target\im-client-0.0.1-SNAPSHOT.jar --server.port=8072 --im.user.id=1002 --im.user.userName=Luffy
```	