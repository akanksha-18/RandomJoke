# Enhanced Random Jokes and Images API

## New Endpoints:

1. GET `/api/images/random`
   - Returns a JSON object with a URL to a random image.
   - Example response: `{ "imageUrl": "https://picsum.photos/id/237/200/200" }`

2. GET `/api/random`
   - Returns a JSON object containing both a random joke and a random image URL.
   - Example response:
     ```json
     {
       "joke": {
         "id": 3,
         "joke": "What do you call a fake noodle? An impasta."
       },
       "imageUrl": "https://picsum.photos/id/237/200/200"
     }
     ```

## Implementation Details:
- Random images are fetched from the Lorem Picsum API (https://picsum.photos).
- The existing jokes data structure is used for random jokes.
- Error handling is implemented to manage potential API failures.

## Challenges Faced:
- Integrating asynchronous API calls with Express routes.
- Ensuring proper error handling for external API requests.
- Combining data from multiple sources (local jokes and external images) in a single response.