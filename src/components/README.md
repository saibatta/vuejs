v-for: it's used to render list of array elements from items in item where items are array list and item is alis to each in it

<MyComponent v-for="item in items" :key="item.id" />
However, this won't automatically pass any data to the component, because components have isolated scopes of their own. In order to pass the iterated data into the component, we should also use props:

Note :It's not recommended to use v-if and v-for on the same element due to implicit precedence.

Summary : When they exist on the same node, v-if has a higher priority than v-for. That means the v-if condition will not have access to variables from the scope of the v-for

Vue is able to detect when a reactive array's mutation methods are called and trigger necessary updates. These mutation methods are:

push()
pop()
shift()
unshift()
splice()
sort()
reverse()

filter(), concat() and slice(), which do not mutate the original array but always return a new array. When working with non-mutating methods, we should replace the old array with the new one:

Vue implements some smart heuristics to maximize DOM element reuse, so replacing an array with another array containing overlapping objects is a very efficient operation.

Sometimes we want to display a filtered or sorted version of an array without actually mutating or resetting the original data. In this case, you can create a computed property that returns the filtered or sorted array.

In situations where computed properties are not feasible (e.g. inside nested v-for loops), you can use a method:

js
const sets = ref([
[1, 2, 3, 4, 5],
[6, 7, 8, 9, 10]
])

function even(numbers) {
return numbers.filter((number) => number % 2 === 0)
}

Be careful with reverse() and sort() in a computed property! These two methods will mutate the original array, which should be avoided in computed getters. Create a copy of the original array before calling these methods
