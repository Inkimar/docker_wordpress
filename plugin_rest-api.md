# rest api 

1. För att få det att fungera: se -> https://stackoverflow.com/questions/34670533/wordpress-rest-api-wp-api-404-error-cannot-access-the-wordpress-rest-api 
2. http://localhost:8080/wp-admin/options-permalink.php 
3. Go to admin, settings, permalinks, choose "inkläggsnamn" 

## denna visar alla möjligheter
1. http://localhost:8080/wp-json/wp/v2 
2. http://localhost:8080/wp-json/wp/v2/posts/?per_page=1
3. /wp/v2/posts/?per_page=1


##
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
