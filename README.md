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
let calculateTotal = (cart) => {
let total =  cart.reduce((acc,item) => (item.price * item.quantity) + acc,0)    
return total +  (total * 10 ) / 100
}

console.log(calculateTotal(cart));
</pre>

<h2>Scenario 2: Form Validation

You’re building a signup form.

Write a function that:
Accepts email and password
Email must include @
Password must be at least 8 characters

Return "Valid" or proper error message</h2>

Solution:

<pre>
function onSubmit() {
  event.preventDefault();
  const name = document.getElementById('name').value
  const email = document.getElementById('email').value
   const password = document.getElementById('password').value
   const result = validateFields(email, password);
  if (result === "Valid") {
    console.log("Form submitted successfully");
  } else {
    console.error(result);
  }
}

function validateFields(email,password) {
  if (!email.includes('@')) {
    return "Invalid email. Must include @";
  }

  if (password.length < 8) {
    return "Password must be at least 8 characters";
  }

  return "Valid";
}
  
 
</pre>

