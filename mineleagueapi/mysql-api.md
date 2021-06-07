# MySQL-API

```bash
MySQL mySQL = MineLeagueAPI.getInstance().getMySQL();

mySQL.executeQuery(String query);
mySQL.executeQuery(String query, List<MySQLParamter> parameters);

# You can execute some asyncron querys with our AsyncMySQLAdapter
AsyncMySQLAdapter asyncMySQLAdapter = mySQL.getAsyncMySQLAdapter();

asyncMySQLAdapter.runAsync(String query, Consumer<ResultSet> resultSetConsumer);
asyncMySQLAdapter.runAsync(String query, List<MySQLParameter> parameters, Consumer<ResultSet> resultSetConsumer);
```

