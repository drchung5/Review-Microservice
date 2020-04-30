# Review Microservice

Listening on port: 9002

### Get all reviews
curl --location --request GET 'http://localhost:9002/reviews'

### Get a review
curl --location --request GET 'http://localhost:9002/reviews/1'

### Add a review
curl --location --request POST 'http://localhost:9002/reviews' \
--header 'Content-Type: application/json' \
--data-raw '{
	"review_text":"Reminds me of evenings in Barcelona. The pulpo is awesome!",
	"rating": 3, 
	"restaurant_id": 3 
}'

### Get all reviews for restaurant
curl --location --request GET 'http://localhost:9002/reviews/restaurant/1'
