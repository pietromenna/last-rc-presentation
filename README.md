#Javascript Quirks taugth by Tom Ballinger! #

## Strange behavior with Closures ##

What does the code below return? Why?

```
 var arr = [];
    for (var i=0;i<3;i++){
        var func = function(){
            console.log(i);
        }
        arr.push(func);
    }
    arr[0]();
```

Test it yourself [here][1]

## Strange behavior with this! ##

```
var Person = function(age){
        this.age = age;
    }
    tom = Person(25);
    console.log(tom.age);
```
Test it yourself [here][2]

Hint: try running `console.log(age);`

## Private members? ##

```
var Person = function(name, age) {
var age = age;
var name = name;

this.getName = function(){
    return age;
}

this.getAge = function(){
    return name;
}
}

var pietro = new Person('Pietro', '32');
console.log(pietro.getName());
console.log(pietro.getAge());
console.log(pietro.name);
console.log(pietro.age);
```

Test it yourself [here][3]

[1]: http://pietro.menna.net.br/last-rc-presentation/closures.html
[2]: http://pietro.menna.net.br/last-rc-presentation/this.html
[3]: http://pietro.menna.net.br/last-rc-presentation/private.html