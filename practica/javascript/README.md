# Javascript exercises

To solve this exercise you can use [codepen](https://codepen.io/) or [codesandbox](https://codesandbox.io/) to execute JS code and then you have to include it in a repository.

## Exercise 1. Objects

Based on the input object we want to access to an specific property called `credit-card`. What should we add in the console.log statement?

```js
const input = {
  name: 'test account',
  firstName: 'test',
  orders: [{
    productId: 'product-1',
    price: 20,
    storeLocale: 'nl',
  },
  {
    productId: 'product-2',
    price: 11,
    storeLocale: 'es',
  }],
  billing: {
    address: 'castellana 41',
    city: 'madrid',
    paymentMethod: {
      'credit-card': '4242424242424242',
    },
  },
};

const solution = input.billing.paymentMethod
// add your solution in the console.log
console.log(solution)
```

## Exercise 2. map

Based on the input object we want to have only the orders without the price info and with the locale at the end of the productId.

```js
const input = {
  name: 'test account',
  firstName: 'test',
  orders: [{
    productId: 'product-1',
    price: 20,
    storeLocale: 'nl',
  },
  {
    productId: 'product-2',
    price: 11,
    storeLocale: 'es',
  },
  {
    productId: 'product-3',
    price: 8,
    storeLocale: 'en',
  }],
  billing: {
    address: 'castellana 41',
    city: 'madrid',
    paymentMethod: {
      'credit-card': '4242424242424242',
    },
  },
};

// add you solution here

const result2 = input.orders.map(elem => ( { productId: elem.productId + elem.storeLocale, } )); 

console.log(result2);
```


## Exercise 3. filter

Based on the input object we want to have the same object but only the orders with a price greater than 10.

```js
const input = {
  name: 'test account',
  firstName: 'test',
  orders: [{
    productId: 'product-1',
    price: 20,
    storeLocale: 'nl',
  },
  {
    productId: 'product-2',
    price: 11,
    storeLocale: 'es',
  },
  {
    productId: 'product-3',
    price: 8,
    storeLocale: 'en',
  }],
  billing: {
    address: 'castellana 41',
    city: 'madrid',
    paymentMethod: {
      'credit-card': '4242424242424242',
    },
  },
};

// add you solution here

input.orders = input.orders.filter((item) => item.price > 10);

```

## Exercise 4. map & filter

Based on the input object we want to have the name of the order productIds with a price greater than 10, and separated by commas.

```js
const input = {
  name: 'test account',
  firstName: 'test',
  orders: [{
    productId: 'product-1',
    price: 20,
    storeLocale: 'nl',
  },
  {
    productId: 'product-2',
    price: 11,
    storeLocale: 'es',
  },
  {
    productId: 'product-3',
    price: 8,
    storeLocale: 'en',
  }],
  billing: {
    address: 'castellana 41',
    city: 'madrid',
    paymentMethod: {
      'credit-card': '4242424242424242',
    },
  },
};

// add you solution here

let res-2 = input.orders.filter((item) -> item.price >10);
let ar = res2.join(",");
console.log(ar);
```

## Exercise 5. reduce

Based on the input object we want the total price of the orders, and include them in the object.

```js
const input = {
  name: 'test account',
  firstName: 'test',
  orders: [{
    productId: 'product-1',
    price: 20,
    storeLocale: 'nl',
  },
  {
    productId: 'product-2',
    price: 11,
    storeLocale: 'es',
  },
  {
    productId: 'product-3',
    price: 8,
    storeLocale: 'en',
  }],
  billing: {
    address: 'castellana 41',
    city: 'madrid',
    paymentMethod: {
      'credit-card': '4242424242424242',
    },
  },
};

// add you solution here

let prices = input.orders.map(item => item.price); 
console.log(prices); 
function suma(a, b){return a+b;} let sum = prices.reduce(suma); 
console.log(sum); 
input.priceSum=sum; console.log(input);

```

