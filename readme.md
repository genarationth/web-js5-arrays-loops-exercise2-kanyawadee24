<img align="right" width="150" height="150" src="https://media-exp1.licdn.com/dms/image/C4E0BAQF7BYCCZt5epw/company-logo_200_200/0?e=2159024400&v=beta&t=qUAFP9bUgBEEXGVQYpUXW1J_OiP8e0r4rFBpqp8OrxA">

# JS-04 Arrays and Loops

 <br/>
 <br/>

Open up a text editor of your choice and complete the following Javascript exercises.

### Exercise #2

#### Part 1

There are three people waiting for the bank. Their names, in order, are Sofia, David, and Juan.
Create an array that has these three names in order.

#### Part 2

Two more people get added to the back of the line - Sara and Augustin.
The first person in line is called to the teller.
What does the queue look like?

#### Part 3

It turns out David was saving a spot for his friend Renata. She shows up and goes behind him in the line. One more person (Elena) shows up and goes to the end of the line.
What does the queue look like? 

//---slice(): Returns a shallow copy of a portion of an array

let fruit_products_slice = ['apple', 'banana', 'mango', 'pear', 'strawberry', 'orange'];

    const newArray = fruit_products_slice.slice(1, 3); // Returns elements at index 1, 2, and 3
    console.log(newArray); // Output: ['banana', 'mango']
    console.log(fruit_products_slice);



//------------------------------------------------------------------------------------------------------------------------------------//

// //---splice(): Changes the contents of an array by removing or replacing existing elements and/or adding new elements.
let fruit_products = ['apple', 'banana', 'mango', 'pear', 'strawberry', 'orange'];

// Replace 'banana' with 'kiwi' at index 1
fruit_products.splice(1, 1, 'kiwi');

console.log(fruit_products); 

// Remove 'mango' and 'pear' from the array starting from index 2
fruit_products.splice(2, 2);

console.log(fruit_products); 

// Add 'grape' and 'pineapple' starting from index 2
fruit_products.splice(2, 0, 'grape', 'pineapple');

console.log(fruit_products); 



// //-----------------------------Real World Splice() & Splice()------------------------//

const cart = ['milk', 'eggs', 'Bananas','shampoo'];

function removeItem(itemName) {
  let itemIndex = cart.indexOf(itemName);
      console.log(itemIndex)
  if (itemIndex === -1) {
    console.error('Item not found in the cart.');
    return;
  }

  const itemToRemove = cart.splice(itemIndex, 1);

  console.log(cart);
  console.log(`Item ${itemToRemove} removed from the cart.`);
}
removeItem('Bananas');
console.log(cart); 