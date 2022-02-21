# Twitter clone backend

# Get started
`cd twitter-clone-backend`
`cargo run`

# list tweets
curl http://localhost:9090/tweets

# get a tweet (return status code: 204 because there is no tweet)
curl http://localhost:9090/tweets/abc

# create a tweet
curl -X POST -d '{"message": "This is a tweet"}' -H "Content-type: application/json" http://localhost:9090/tweets

# delete a tweet (return status code: 204 in any case)
curl -X DELETE http://localhost:9090/tweets/abc

# list likes from a tweet
curl http://localhost:9090/tweets/abc/likes

# add one like to a tweet
curl -X POST http://localhost:9090/tweets/abc/likes

# remove one like to a tweet
curl -X DELETE http://localhost:9090/tweets/abc/likes
