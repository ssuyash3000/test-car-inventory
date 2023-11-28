**Interview - 1**
Task - 
Step 1:
Create a component to add a car into a list of Cars.
Fields that are required as attributes of a car are  Name, Model and Quantity.

Step 2:
Create another component which will display the list of cars.

Step 3:
On adding the car of same Brand and Model, quantity should be added in existing Car Object instead of creating a new Car Object in the list

**Interview - 2**
Task - Implement 2 Input tags in different component, 
When the number input is done is input tag of first component, value of input tag in 2nd component should get updated 
in sync with the value/2 of value input in 1st tag,
and similarly when input to be done in 2nd tag, value in first should update with value * 2 in sync.
Then some baisc react question 
Like what is useEffect redux 

and then a javascript coding question similar to 
Flatten an array problem statement 

I was supposed to get the sum of the numbers out the following object 
let obj = { a: { x: [1, 2, 3, 4, 5, { m: [1, 2, 3, 4, 5, 8] }] } };
Solved this problem too 

Following is the code that I wrote 
```
let obj = { a: { x: [1, 2, 3, 4, 5, { m: [1, 2, 3, 4, 5, 8] }] } };
function sumofobj(obj) {
  let sum = 0;
  if (Array.isArray(obj)) {
    for (let i = 0; i < obj.length; i++) {
      if (typeof obj[i] === "number") {
        sum += obj[i];
      } else {
        sum += sumofobj(obj[i]);
      }
    }
  } else {
    let keys = Object.keys(obj);
    for (let i = 0; i < keys.length; i++) {
      sum += sumofobj(obj[keys[i]]);
    }
  }
  return sum;
}

let value = sumofobj(obj);
console.log(value);

```
**Interview - 3**
Task - 
Make change in the project of Interview - 1
Make change in carList component such that it renders the car list in tabular format 
Implement a sell car page where selection of cars to be sold can be done using the dropdown menu 
and number of car sold be input in input tag.
When user hits sell car button number of car should get updated in the car list 
and if the number car input by the user exceeds the number of car in the car list, then there should be a message displayed that 
That much car is not in the inventory
