wx-xml2js
===========

Copy xml2js and adapt it to wechat.

Description
===========

For options, please refer to: [xml2js](https://www.npmjs.com/package/xml2js)

----------------------
Convert xml to json:

```javascript
import xml2js from 'wx-xml2js'
xml2js.parseString(xml, (err, result) => {
  if(err) {
    // some thing
  }
})
```

----------------------
Convert json to xml:

```javascript
import xml2js from 'wx-xml2js'
var jsonData = '<xml><ToUserName>abc</ToUserName></xml>'
var builder = new xml2js.Builder({
  rootName: 'xml',
  headless: true,
  cdata: true,
  renderOpts: {
    pretty: true,
    indent: '',
    newline: '' 
  }
});
var xmlData = builder.buildObject(jsonData);
```