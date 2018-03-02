# Mongo Diary

用来记录每天学习mongoDB的心得。
跟做一些小项目。

## Project
* 基础
  * 记录好友生日

    > 需求： 将朋友的生日录入数据库

    主要考察数据库的写入以及日期格式的处理


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
        db.<collection>.insert({<property>:'<value>'})
        ```
      * Delete table
        ```
        db.<collection>.drop()
        ```
  * ### Documents(Data)
    * Create
      * Insert Document
        ```
        db.<collection>.insert({<property>:'<value'})
        ```
      * Insert Multiple Documents
        ```
        db.<collection>.insert(
            [
              {<property>:'<value>'},
              {<property>:'<value>'},
            ]
          )
        ```
    * Query
      * List all documents
        ```
        use <database>
        db.<collection>.find()
        ```
      * List specific document
        ```
        use <database>
        db.<collection>.find({<property>:'<value>'})
        ```
      * List spcific documents with requirement
        ```javascript
        //equals
        db.<collection>.find({<property>:{ $in ['<value1>', '<value2>'] } } )
        //or
        db.<collection>.find({<property>:{ $or ['<value1>','<value2>'] } } )
        //operation
        db.<collection>.find({<property>:{ $lt : <number>} } ) //less than
        db.<collection>.find({<property>:{ $gt : <number>} } ) //great than
        //RegExp
        db.<collection>.find({<property>:{$regex: /d/} } )
