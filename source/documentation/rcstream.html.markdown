---
category: documentation
title: RCStream
date: 2014/05/09
---

Lorem ipsum.

```javascript
var socket = io.connect( '/rc' );

function log( text ) {
  if ( typeof text !== 'string' ) {
    text = JSON.stringify( text, null, 2 );
  }
  pre = document.createElement( 'pre' );
  pre.innerText = text;
  document.body.insertBefore( pre, document.querySelector( 'script' ) );
  console.log( text );
}

socket.on( 'connect', function () {
  log( 'connected!' );
  socket.emit( 'subscribe', [ 'enwiki', 'bgwiki' ] );
} );

socket.on( 'change', function ( data ) {
  log( data );
} );
```
