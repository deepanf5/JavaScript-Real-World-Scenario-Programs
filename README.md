# JavaScript-Real-World-Scenario-Programs


<h2>1.You get data from an API: filter by Active users only and return their names</h2>

<pre>
const users = [
  { id: 1, name: "John", active: true },
  { id: 2, name: "Sara", active: false },
  { id: 3, name: "Mike", active: true }
];
</pre>

Solution:  
<pre>
const users = [
  { id: 1, name: "John", active: true },
  { id: 2, name: "Sara", active: false },
  { id: 3, name: "Mike", active: true }
];

const filterBy = (users) => {
     return users.filter((user) =>  user.active).map((user) => user.name)
}
console.log(filterBy(users))

</pre>

<h2>2.Calculate the total cart value 
Add 10% tax
Return the final amount
from this cart item </h2>

<pre>
const cart = [
  { name: "Shirt", price: 20, quantity: 2 },
  { name: "Shoes", price: 50, quantity: 1 },
  { name: "Cap", price: 10, quantity: 3 }
];</pre>

Solution: 

<pre>
const cart = [
  { name: "Shirt", price: 20, quantity: 2 },
  { name: "Shoes", price: 50, quantity: 1 },
  { name: "Cap", price: 10, quantity: 3 }
];

let calculateTotal = (cart) => {
let total =  cart.reduce((acc,item) => (item.price * item.quantity) + acc,0)    
return total +  (total * 10 ) / 100
}

console.log(calculateTotal(cart));
</pre>


