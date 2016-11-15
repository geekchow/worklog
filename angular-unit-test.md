the $provide usage:
https://gist.github.com/demisx/9605099


mock translate filter
```
var mockFilter = function() {
    return 'whatyouwantittoreturn';
};

beforeEach(function() {
    module(function($provide) {
        $provide.value('dateFilter', mockFilter );
    });
});
```
