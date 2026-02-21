# JavaScript-Real-World-Scenario-Programs


<h1>1.You get data from an API: filter by Active users only and return their names</h1>

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



