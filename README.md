# Call-apply-and-bind
Coding using Javascript call, apply and bind 

// Call Method
var obj = {num:6};

var functionAdd = function( x, y, z ){
		return this.num + x + y + z; 
}

console.log(functionAdd.call( obj, 2, 4, 6));  // 18

// Apply method
let obj = {num:6};

let functionAdd = function( x, y, z ){
		return this.num + x + y + z; 
}
let arr= [2, 4, 6];
console.log(functionAdd.apply( obj, arr)); //18

// Bind method
let obj = {num:6};

let functionAdd = function( x, y, z ){
		return this.num + x + y + z; 
}
var bound = functionAdd.bind(obj);
console.log(bound( 1, 2, 3)); //12
