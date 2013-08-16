Cache.js
========

A client side storage abstraction.

Uses `localStorage` by default, fallbacks to [jQuery.cookie](https://github.com/carhartl/jquery-cookie), if available.

### Usage

    Cache('my_cache_key').memorize({
        name: 'cachejs',
        creator: 'jkempff'
    });

    Cache('my_cache_key').remember().name; // 'cachejs'

or

    var myCache = Cache('my_cache_key');
    myCache.memorize({
        name: 'cachejs',
        thisTime: 'stored in a variable'
    });

    myCache.remember().thisTime;; // 'stored in a variable'