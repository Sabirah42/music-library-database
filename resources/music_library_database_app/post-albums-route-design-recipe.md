POST /albums Route Design Recipe
1. Design the Route Signature

HTTP method: POST

Path: /albums

Query parameters: none

Body parameters:
    title=Voyage
    release_year=2022
    artist_id=2

2. Design the Response (i.e. behaviours)

When 'POST /albums' body params =
    title=Voyage
    release_year=2022
    artist_id=2

Response = 200 OK (no content)

3. Write Examples

#1
Request: POST /albums
Expected response: Response for 200 OK - no other content returned
 
#2
Request: GET /albums/2
Expected response: Response for 200 OK - returns album where artist_id=2
 
4. Encode Examples as Tests
This will include the request and expected response from above.

# EXAMPLE
# file: spec/integration/application_spec.rb

require "spec_helper"
require "rack/test" 
require_relative '../../app'

describe Application do
  include Rack::Test::Methods

  let(:app) { Application.new }

# create a context for every route
  context "GET /" do
    it 'returns 200 OK' do
      # Assuming the post with id 1 exists.
      response = get('/posts?id=1')

      expect(response.status).to eq(200)
      # expect(response.body).to eq(expected_response)
    end

    it 'returns 404 Not Found' do
      response = get('/posts?id=276278')

      expect(response.status).to eq(404)
      # expect(response.body).to eq(expected_response)
    end
  end
end
5. Implement the Route
Write the route and web server code (in your application.rb file) to implement the route behaviour.
