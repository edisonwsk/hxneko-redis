# hxneko-redis #

This is a client library for accessing a Redis key value store from
haxe/neko.

More info on redis can be found [here](http://redis.io/).
The redis interface is described [here](http://redis.io/commands).
More info on haxe can be found [here](http://haxe.org/).

There is a short example below.  There is a more extensive example in the repo at /example/src/Main.hx.

# Example #

```
import redis.Redis;
    
static function main()
{
    var db = new Redis("localhost");        // instantiate an object
    
    db.set("key1", "value1");               // set some keys
    db.set("key2", "value2");
    
    trace(db.get("key2"));                  // outputs: "value2"
    trace(db.get("key1"));                  // outputs: "value1"
}
```