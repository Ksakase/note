
### 2022年7月3日13時21分：mysql のログバッファのサイズを確認したい
```
# dockerコンテナ起動
docker up -d
docker-compose run web rails db:create

show variables like 'innodb_log_buffer_size'
-- > 16MB
Variable_name	Value
innodb_log_buffer_size	16777216

# refs 
https://dev.mysql.com/doc/refman/5.7/en/innodb-redo-log-buffer.html
→Thus, if you have transactions that update, insert, or delete many rows, increasing the size of the log buffer saves disk I/O.
```
