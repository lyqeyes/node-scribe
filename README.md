# node-scribe
Scribe client for node.js.
基于node-scribe改动, 解决中文乱码的问题

## Installation
    $ npm install @mx/scribe
    
## Basic example
Example of sending log entries to scribe server.

    var Scribe = require('@mx/scribe').Scribe;

    var scribe = new Scribe("localhost", 1234, {autoReconnect:true});

    scribe.open(function(err){

      if(err) {
        return console.log(err);
      }

      scribe.send("foocategory", "foomessage");

      scribe.close();

    });
