---
category: documentation
title: RCStream
description: Lorem ipsum dolor sit amet, consectetur adipiscing elit. Curabitur non suscipit massa. Donec vitae arcu pellentesque, scelerisque turpis ut, vulputate urna. Nunc semper hendrerit sollicitudin. Vivamus lobortis, dui luctus rhoncus fringilla, elit enim ultrices nibh, ut rutrum massa lacus quis est.
date: 2014/05/09
---

 Etiam mollis auctor quam, nec eleifend risus convallis sed. Nam ante purus, dictum vel lobortis ut, pharetra vitae nisl. Suspendisse bibendum ante a consectetur sodales. Nunc sed scelerisque ante. Vivamus ut eros eget risus malesuada eleifend id non odio. Proin dolor felis, tempus ut justo et, facilisis congue est. Morbi molestie magna nec nisl mollis, eget cursus risus mollis. Duis sit amet nulla lacus. Sed ornare convallis tellus non tincidunt.

Vestibulum lectus ligula, ultricies quis iaculis eleifend, molestie ut mauris. Vestibulum interdum leo vel fringilla pellentesque. Fusce vel neque nibh. Ut eget dapibus tortor, sed consequat purus. Integer rhoncus ultrices lacus accumsan sollicitudin. Nullam nec turpis id augue laoreet imperdiet. Duis vitae lorem ut ligula feugiat eleifend ac et lacus. Pellentesque interdum dui ac ipsum venenatis, eu tincidunt est commodo. Nulla sollicitudin ultrices purus, et egestas ante convallis non. Duis vel condimentum nisl, at rutrum magna. Vestibulum luctus tristique viverra. Curabitur vitae facilisis quam, et euismod mi. Nulla tincidunt viverra risus, et placerat mi varius non. Cum sociis natoque penatibus et magnis dis parturient montes, nascetur ridiculus mus. Aliquam non diam eros. 

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
