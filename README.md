#Part 1: Questions

1. Explain the output of the following code and why

```jsx
setTimeout(function() {
	console.log("1");
}, 100);  

console.log("2");
```

Ans:

Output: 

"2"
"1"

Explaination: prints 1 after 100 milliseconds but 2 will be printed first because no timer set for this.

2. Explain the output of the following code and why

```jsx
function foo(d) {
	if(d < 10) {
		foo(d+1);
	}
	console.log(d);
}

foo(0);
```

Ans:

Output:

10
9
8
7
6
5
4
3
2
1
0

Explaination: Recursive method call which starts from 0 and stops at 10.

3. If nothing is provided to `foo` we want the default response to be `5`. Explain the potential issue with the following code:

```jsx
function foo(d) {
	d = d || 5;
	console.log(d);
}
```

Ans:

Fixed Code:

```jsx
function foo(d = 5) {
	d = d || 5;
	console.log(d);
}
```

Explaination: Value can be intialise with default value then if nothing is passed in foo method then 5 will be printed as default.

4. Explain the output of the following code and why

```jsx
function foo(a) {
	return function(b) {
		return a + b;
	}
}

const bar = foo(1);

console.log(bar(2))
```

Ans:

Output: 3

Explaination:  One method returns another method with different value as lamda expression


5. Explain how the following function would be used

```jsx
function double(a, done) {
	setTimeout(function() {
		done(a * 2);
	}, 100);
}
```
Ans:

Code:

```jsx
function done(b){
return b;
}

const re = done(1);
double(1,re);
```
