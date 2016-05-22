Blocking Code
Create a text file named input.txt with some content

var fs = require("fs");

var data = fs.readFileSync('input.txt');

console.log(data.toString());
console.log("Program Ended");
Now run the main.js to see the result:

$ node main.js

===============
Non-Blocking Code 
Create a text file named input.txt with some content


var fs = require("fs");

fs.readFile('input.txt', function (err, data) {
    if (err) return console.error(err);
    console.log(data.toString());
});

console.log("Program Ended");
