## Drupal 8 Restful API & Services

Here there is a good video tutorial by MediaCurrent about Restful API in Drupal 8 Core

http://www.youtube.com/watch?v=TLHP9doaZ98

I the tutorial, adsasd used [Dev HTTP Client Chrome App](https://chrome.google.com/webstore/detail/dev-http-client/aejoelaoggembcahagimdiliamlcdmfm) for making HTTP requests.

When requesting for entities (content), GET was used

    GET <YOUR-DOMAIN.COM>/entity/node/1

with this HEADER:

    Accept:application/json

When requesting for entity (content) creation, POST was used

    POST <YOUR-DOMAIN.COM>/entity/node

with this two HEADERS:

    Content-Type:application/hal+json
    X-CSRF-Token:<YOUR-TOKEN>

Token can be obtained, when logged, by visiting

    http://<YOUR-DOMAIN.COM>/rest/session/token

Here is a HAL+json code needed to create a content of a basic content type:

    {
      "title":[
        {
        "value":"Test"
        }
      ],
      "_links": {
        "type": {
          "href": "http://<YOUR-DOMAIN.COM>/rest/type/node/your-content-type"
        }
      }
    }


Source: [Drupal 8 Restful Services](http://www.mediacurrent.com/blog/drupal-8-restful-services)



