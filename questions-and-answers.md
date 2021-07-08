问：redolog 都长什么样

答：

---

问：sql语句回表次数

CREATE TABLE `t` (
  `id` int NOT NULL,
  `a` int DEFAULT NULL,
  `b` int DEFAULT NULL
  PRIMARY KEY (`id`),
  KEY `a` (`a`),
  KEY `b` (`b`)
) ENGINE=InnoDB DEFAULT CHARSET=utf8

插入10万条数据
for(int i=1; i<100000; i++){
 insert table t values(i, i, i);
}

select * from a where a = 1 会回表1次，
那么 select * from a where a > 100 and a <1000 回表的次数是多少次

答：900次

---
