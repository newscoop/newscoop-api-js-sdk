Newscoop API JS-SDK
=============================

[Newscoop][1] is the open content management system for professional journalists.

Features for the modern newsroom include multiple author management,
issue-and-section based publishing, geolocation and multilingual content 
management. The enterprise-standard journalist’s dashboard and a templating 
engine supporting anything from HTML5 to mobile complete this fast 
production and publishing system.

This library allows for access to [Newscoop REST API][2] (codename gimme).

## Installation

    <script src="newscoop.js"></script>

## Usage

```javascript
var api = new NewscoopRestApi('http://newscoop.dev/api');

api.getResource('/articles', {'type': 'news'})
    .setItemsPerPage(5)
    .setOrder({'number': 'asc'})
    .makeRequest(function(res){
        // callback
    });

```

## More Information

Sdk makes XMLHttpRequest to apiEndpoint, make sure that apiEndpoint have your host in "access-control-allow-origin" response header.

Read the Newscoop REST API [documentation][2] for more information.

## License

Newscoop API JS-SDK is licensed under the GPL3 license.

[1]: http://www.sourcefabric.org/en/newscoop/
[2]: https://wiki.sourcefabric.org/display/CS/Newscoop+REST+API+Reference