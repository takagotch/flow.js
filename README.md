### flow.js
--- 
https://github.com/flowjs/flow.js

```
bower install flow.js#~2
git clone https://github.com/flowjs/flow.js

cd flow.js
npm install
grunt karma:watch
grunt karma:watch --browsers=Firefox, Chrome
curl https://saucelabs.com/docs/connect
grunt test --sauce-local=true --sauce-username=*** --sausce=access-key=***
```

```js
var flow = new Flow({
  target: '/api/photo/redeem-upload-token',
  query: {upload_token:'my_token'}
});
if(!flow.support) location.href = '/some-old-crappy-uploadder';

flow.assignBrowse(document.getElementById('browseButton'));
flow.assignDrop(document.getElementById('dropTarget'));

flow.on('fileAdded', function(file, event){
  console.log(file, event);
});
flow.on('fileSuccess', function(file,message){
  console.log(file,message);
});
flow.on('fileError', function(file, message){
  console.log(file, message);
});

var r = new Flow({opt1: 'val', ...});
```

```
```

