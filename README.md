# Review Microservice

Listening on port: 9000

### Get all reviews
curl --location --request GET 'http://localhost:9000/reviews'

### Get a review
curl --location --request GET 'http://localhost:9000/reviews/1'

### Add a review
curl --location --request POST 'http://localhost:9000/reviews' \
--header 'Content-Type: application/json' \
--data-raw '{
	"review_text":"Reminds me of evenings in Barcelona. The pulpo is awesome!",
	"rating": 3, 
	"restaurant_id": 3 
}'

### Get all reviews for restaurant
curl --location --request GET 'http://localhost:9000/reviews/restaurant/1'

### Access Swagger UI (in a browser)
http://localhost:9000/swagger-ui.html

### Access Database (h2) Console (in a browser)
http://localhost:9000/h2-console