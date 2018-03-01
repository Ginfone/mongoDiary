# mongoDiary

用来记录每天学习mongoDB的心得。
跟做一些小项目。

## Project
* 好友生日提醒

  > 需求： 将朋友的生日录入数据库


## Note
  * ### Database
    * Create
      * Create & Switch Database
        ```
        use <database>
        ```
    * Query
      * To display database you are using
        ```
        db
        ```
      * To display all database
        ```
        show dbs
        ```
        or

        ```
        show databases
        ```
    * Delete
      * Delete
        ```
        use <database>
        db.dropDatabase();
        ```
  * ### Collections (Tables)
    * Create
      * Create table
        ```
        db.<collection>.insert({<property>:<value>})
        ```
