# Mongo Diary

用来记录每天学习mongoDB的心得。
跟做一些小项目。

## Project
* 基础
  * 记录好友生日

    > 需求： 将朋友的生日录入数据库

    主要考察数据库的写入以及日期格式的处理


## Theory
  * no predefined schema
  > which makes more flexible.

  * It's document-oriented data model makes it easier for it to split up data across multiple server
  * Case-sentive && Type-sensitive

  * Subcolletion
  > Seperater collection by . character.
    subcollection is a great way to store data in mongoDB. For example, blog.posts , blog.authors

  * One database for one application is recommend.
  * To keep it simple ,try to just use lowercase character.


## Usage
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
        db.<collection>.insert({<key>:'<value>'})
        ```
      * Delete table
        ```
        db.<collection>.drop()
        ```
  * ### Documents(Data)
    * Create
      * Insert Document
        ```
        db.<collection>.insert({<key>:'<value'})
        ```
      * Insert Multiple Documents
        ```
        db.<collection>.insert(
            [
              {<key>:'<value>'},
              {<key>:'<value>'},
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
        db.<collection>.find({<key>:'<value>'})
        ```
      * List spcific documents with requirement
        ```javascript
        //equals
        db.<collection>.find({<key>:{ $in ['<value1>', '<value2>'] } } )

        //or
        db.<collection>.find({<key>:{ $or ['<value1>','<value2>'] } } )

        //operation
        db.<collection>.find({<key>:{ $lt : <number>} } ) //less than
        db.<collection>.find({<key>:{ $gt : <number>} } ) //great than

        //RegExp
        db.<collection>.find({<key>:{$regex: /pattern/} } )
        ```

## mongoose
  * mongoose will makes the correct plural of the collection.
