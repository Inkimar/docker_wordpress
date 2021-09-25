# rest api 
https://webdesign.tutsplus.com/tutorials/how-to-use-the-wordpress-rest-api-a-practical-tutorial--cms-33566


curl https://example.com/wp-json/wp/v2/posts 

http://yoursite.com/wp-json/wp/v2 

## första inlägget 
-> http://localhost:8080/?p=1 

http://localhost:8080/?p=7

### 
GET /wp/v2/posts


1. curl -X GET http://yoursite.com/wp-json/wp/v2/posts
2. curl -X GET http://localhost:8080/wp-json/wp/v2/posts 
3. curl http://localhost:8080/wp/v2/posts 
4. curl http://localhost:8080/wp/v2/pages


## med inlogg
curl -v -X GET --user ingimar:ingimar -i http://localhost:8080/wp-json/wp/v2/posts 

# gutenberg -> bara '2 stjärnor' från användarna, mest '1'or

https://sv.wordpress.org/plugins/gutenberg/
