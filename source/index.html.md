---
title: API Reference

language_tabs:
  - shell
  - javascript
  - swift

toc_footers:
  - <a href='#'>Sign Up for a Developer Key</a>
  - <a href='https://github.com/tripit/slate'>Documentation Powered by Slate</a>

includes:
  - errors

search: true
---

# Introduction

Welcome to the i am a Kid API! You can use our API to access iamakid API endpoints, which can get information on various cats, kittens, and breeds in our database.

We have language bindings in Shell, Ruby, Python and JavaScript! You can view code examples in the dark area to the right, and you can switch the programming language of the examples with the tabs in the top right.

This example API documentation page was created with [Slate](https://github.com/tripit/slate).


# Content

## Get All Content

```shell
curl "https://vma6go3pve.execute-api.us-east-1.amazonaws.com/Dev/iamakidalldata"
```

```javascript
var request = require("request");

var options = { method: 'GET',
  url: 'https://vma6go3pve.execute-api.us-east-1.amazonaws.com/Dev/iamakidalldata',
  headers: 
   { 'postman-token': 'e8e8b9c2-bc13-b743-eea4-c51cd284cf78',
     'cache-control': 'no-cache' } };

request(options, function (error, response, body) {
  if (error) throw new Error(error);

  console.log(body);
});
```
```swift
import Foundation

let headers = [
  "cache-control": "no-cache",
  "postman-token": "68537c46-ccc4-f1e0-6c39-0e726bfc281a"
]

let request = NSMutableURLRequest(url: NSURL(string: "https://vma6go3pve.execute-api.us-east-1.amazonaws.com/Dev/iamakidalldata")! as URL,
                                        cachePolicy: .useProtocolCachePolicy,
                                    timeoutInterval: 10.0)
request.httpMethod = "GET"
request.allHTTPHeaderFields = headers

let session = URLSession.shared
let dataTask = session.dataTask(with: request as URLRequest, completionHandler: { (data, response, error) -> Void in
  if (error != nil) {
    print(error)
  } else {
    let httpResponse = response as? HTTPURLResponse
    print(httpResponse)
  }
})

dataTask.resume()
```
> The above command returns JSON structured like this:

```json
[
  {
      "StoryAudioSize": 5191771,
      "StoryImageUrl": "https://iamakid.s3-accelerate.amazonaws.com/story-images/Beauty%20And%20The%20Beast.png?AWSAccessKeyId=ASIAJEJ5MYKJWYHT2WSA&Expires=1489668550&Signature=nV2fVVjOFKohnUntXIoPwHmEn9g%3D&x-amz-security-token=FQoDYXdzEEYaDIZKB5isk%2FKWCnKCKyLmAXxt1odw0l3DfR8p%2Bh3Kgq98eOVceG%2FyTKJHf7ymwCVyaw7KXqf1VMJ3vxp2pKnWQmHwSDErzAwVA5UQamBvNvWkh3UOxajG2ZgQ9p6WMXldVvHWKM6ZQQPI%2FHQGkIErRR9OHA7%2FjjLZ8j4JBMNZMS8X3bZH9owKsa7xSIV82uCOThspp0c%2BA9Aabxbd5W4p6H9huR838gIQm%2F%2Fotmcb3T7%2Fh8ydF721xOu%2FVj1Hszdn%2F2rI3wz6BpqUBNqRuU53BoLAATfZ5N5eNvdkvMDB%2Fvl%2ButFD7JcyuicsrZMXg3uF%2FIcSjLVlKOaRhcYF",
      "StoryName": "Beauty And The Beast",
      "StoryTextSize": 1656,
      "StoryImageSize": 136975,
      "StoryTextUrl": "https://iamakid.s3-accelerate.amazonaws.com/story-text/Beauty%20And%20The%20Beast.txt?AWSAccessKeyId=ASIAJEJ5MYKJWYHT2WSA&Expires=1489668548&Signature=nPm0iF1ssyDSvMF6ZKfB7KjE6i4%3D&x-amz-security-token=FQoDYXdzEEYaDIZKB5isk%2FKWCnKCKyLmAXxt1odw0l3DfR8p%2Bh3Kgq98eOVceG%2FyTKJHf7ymwCVyaw7KXqf1VMJ3vxp2pKnWQmHwSDErzAwVA5UQamBvNvWkh3UOxajG2ZgQ9p6WMXldVvHWKM6ZQQPI%2FHQGkIErRR9OHA7%2FjjLZ8j4JBMNZMS8X3bZH9owKsa7xSIV82uCOThspp0c%2BA9Aabxbd5W4p6H9huR838gIQm%2F%2Fotmcb3T7%2Fh8ydF721xOu%2FVj1Hszdn%2F2rI3wz6BpqUBNqRuU53BoLAATfZ5N5eNvdkvMDB%2Fvl%2ButFD7JcyuicsrZMXg3uF%2FIcSjLVlKOaRhcYF",
      "StoryAudioUrl": "https://iamakid.s3-accelerate.amazonaws.com/story-audio/Beauty%20And%20The%20Beast.mp3?AWSAccessKeyId=ASIAJEJ5MYKJWYHT2WSA&Expires=1489668553&Signature=WTlYfL3GsfCscollSxmF5%2BGP3aw%3D&x-amz-security-token=FQoDYXdzEEYaDIZKB5isk%2FKWCnKCKyLmAXxt1odw0l3DfR8p%2Bh3Kgq98eOVceG%2FyTKJHf7ymwCVyaw7KXqf1VMJ3vxp2pKnWQmHwSDErzAwVA5UQamBvNvWkh3UOxajG2ZgQ9p6WMXldVvHWKM6ZQQPI%2FHQGkIErRR9OHA7%2FjjLZ8j4JBMNZMS8X3bZH9owKsa7xSIV82uCOThspp0c%2BA9Aabxbd5W4p6H9huR838gIQm%2F%2Fotmcb3T7%2Fh8ydF721xOu%2FVj1Hszdn%2F2rI3wz6BpqUBNqRuU53BoLAATfZ5N5eNvdkvMDB%2Fvl%2ButFD7JcyuicsrZMXg3uF%2FIcSjLVlKOaRhcYF"
    },...
]
```

This endpoint retrieves all content for all the stories.

### HTTP Request

`GET https://vma6go3pve.execute-api.us-east-1.amazonaws.com/Dev/iamakidalldata`

### Query Parameters

<!--Parameter | Default | Description
--------- | ------- | -----------
include_cats | false | If set to true, the result will also include cats.
available | true | If set to false, the result will include kittens that have already been adopted.-->

<aside class="success">
Remember — It is a get request
</aside>

## Get a Specific Kitten

```shell
curl "https://vma6go3pve.execute-api.us-east-1.amazonaws.com/Dev/writetoddb"
```

```javascript
var request = require("request");

var options = { method: 'GET',
  url: 'https://vma6go3pve.execute-api.us-east-1.amazonaws.com/Dev/writetoddb',
  headers: 
   { 'postman-token': 'c8d55dc2-75ee-98ee-e9c3-ee6e5c7ce35e',
     'cache-control': 'no-cache' } };

request(options, function (error, response, body) {
  if (error) throw new Error(error);

  console.log(body);
});
```
```swift
import Foundation

let headers = [
  "cache-control": "no-cache",
  "postman-token": "5896e215-d5f8-293d-b8dc-105b012d0f11"
]

let request = NSMutableURLRequest(url: NSURL(string: "https://vma6go3pve.execute-api.us-east-1.amazonaws.com/Dev/writetoddb")! as URL,
                                        cachePolicy: .useProtocolCachePolicy,
                                    timeoutInterval: 10.0)
request.httpMethod = "GET"
request.allHTTPHeaderFields = headers

let session = URLSession.shared
let dataTask = session.dataTask(with: request as URLRequest, completionHandler: { (data, response, error) -> Void in
  if (error != nil) {
    print(error)
  } else {
    let httpResponse = response as? HTTPURLResponse
    print(httpResponse)
  }
})

dataTask.resume()
```
> The above command returns JSON structured like this:

```json
{
  "Message": "Successfully Written to DynamoDB"
}
```

This endpoint allows the copying of all data from buckets to DB.

<aside class="warning">Inside HTML code blocks like this one, you can't use Markdown, so use <code>&lt;code&gt;</code> blocks to denote code.</aside>

### HTTP Request

`GET https://vma6go3pve.execute-api.us-east-1.amazonaws.com/Dev/writetoddb`

### URL Parameters

<!--Parameter | Description
--------- | -----------
ID | The ID of the kitten to retrieve-->
