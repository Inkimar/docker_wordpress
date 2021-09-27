#  mysql> show tables;
```
+-----------------------+
| Tables_in_exampledb   |
+-----------------------+
| wp_commentmeta        |
| wp_comments           |
| wp_links              |
| wp_options            |
| wp_postmeta           |
| wp_posts              |
| wp_term_relationships |
| wp_term_taxonomy      |
| wp_termmeta           |
| wp_terms              |
| wp_usermeta           |
| wp_users              |
+-----------------------+
12 rows in set (0.00 sec)
```

## tabellerna wp_posts & wp_postmetadata

```
mysql> desc wp_posts;
+-----------------------+---------------------+------+-----+---------------------+----------------+
| Field                 | Type                | Null | Key | Default             | Extra          |
+-----------------------+---------------------+------+-----+---------------------+----------------+
| ID                    | bigint(20) unsigned | NO   | PRI | NULL                | auto_increment |
| post_author           | bigint(20) unsigned | NO   | MUL | 0                   |                |
| post_date             | datetime            | NO   |     | 0000-00-00 00:00:00 |                |
| post_date_gmt         | datetime            | NO   |     | 0000-00-00 00:00:00 |                |
| post_content          | longtext            | NO   |     | NULL                |                |
| post_title            | text                | NO   |     | NULL                |                |
| post_excerpt          | text                | NO   |     | NULL                |                |
| post_status           | varchar(20)         | NO   |     | publish             |                |
| comment_status        | varchar(20)         | NO   |     | open                |                |
| ping_status           | varchar(20)         | NO   |     | open                |                |
| post_password         | varchar(255)        | NO   |     |                     |                |
| post_name             | varchar(200)        | NO   | MUL |                     |                |
| to_ping               | text                | NO   |     | NULL                |                |
| pinged                | text                | NO   |     | NULL                |                |
| post_modified         | datetime            | NO   |     | 0000-00-00 00:00:00 |                |
| post_modified_gmt     | datetime            | NO   |     | 0000-00-00 00:00:00 |                |
| post_content_filtered | longtext            | NO   |     | NULL                |                |
| post_parent           | bigint(20) unsigned | NO   | MUL | 0                   |                |
| guid                  | varchar(255)        | NO   |     |                     |                |
| menu_order            | int(11)             | NO   |     | 0                   |                |
| post_type             | varchar(20)         | NO   | MUL | post                |                |
| post_mime_type        | varchar(100)        | NO   |     |                     |                |
| comment_count         | bigint(20)          | NO   |     | 0                   |                |
+-----------------------+---------------------+------+-----+---------------------+----------------+
23 rows in set (0.00 sec)
```

**Det som sparas när jag lägger in Fjäril med följande attr.**
1. Alt Text : alt-butterfly
2. Title : title butterfly
3. Caption: this is the captioin
4. Description: this is the description 
5. File URL: http://localhost:8080/wp-content/uploads/2021/09/butterfly-1373983511sKq.jpg 

följande sparas: `mysql> select * from wp_posts where ID=34;`
1. ID = 34
2. post_author = 1 (pekar på 'ingimar' i tabellen = xxx )
3. post_date = 2021-09-27 15:12:43 (date-time, lokaltid)
4. post_date_gmt =2021-09-27 14:12:43 (date-time, lokaltid)
5. post_content = 'this is the description'
6. post_title = 'title butterfly'
7. post_excerpt = 'this is the caption' 
8. post_status ='inherit'
9. comment_status = 'open'
10. ping_status ='closed'
11. post_name ='butterfly-1373983511skq'
12. **post_modified** = 2021-09-27 15:13:42
13. **post_modified_gmt** = 2021-09-27 14:13:42
14. guid = 'http://localhost:8080/wp-content/uploads/2021/09/butterfly-1373983511sKq.jpg'
15. menu order = 0
16. post_type=attachment
17. post_mime_type=image/jpeg
18. comment_count=0



-----------
Går det att ändra 'Slug' för bilder ?
