# Skilly

This project was generated with Node.js

## Development server

Run `node index.js` for a dev server. Navigate to `http://localhost:3000/`. The application will automatically reload if you change any of the source files.

## Server params

Send the URL encoded.


Javascript
```var myUrl = "http://www.image.com/?username=unknown&password=unknown";
var encodedURL= "http://www.foobar.com/foo?imageurl=" + encodeURIComponent(myUrl);
```


PHP
```
echo urlencode("http://www.image.com/?username=unknown&password=unknown");
```
