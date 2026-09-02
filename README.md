# Mern-stack
# This time it will happen
>Js 
// call back functions ,promises (.then  and .catch ,.asynch)
**// normal Function**
function selectproduct( ) {
  setTimeout( ()=>{
console.log("product selected")
},2000)
}


 function addtocart( ) {
  setTimeout( ()=>{
console.log("product added")
},3000)
}

function payment( ) {
  setTimeout( ()=>{
console.log("product payment done")
},4000)
}

function delivered( ) {
  setTimeout( ()=>{
console.log("product delevered")
},3000)
}

selectproduct()
addtocart()
payment()
delivered()



**// Callback Functions**

function selectProduct(cb) {
  setTimeout(() => {
    console.log("Product selected");
    cb();
  }, 2000);
}

function addToCart(cb) {
  setTimeout(() => {
    console.log("Product added to cart");
    cb();
  }, 3000);
}

function payment(cb) {
  setTimeout(() => {
    console.log("Product payment done");
    cb();
  }, 4000);
}

function delivered() {
  setTimeout(() => {
    console.log("Product delivered");
  }, 3000);
}


// Calling using callbacks

selectProduct(() => {
  addToCart(() => {
    payment(() => {
      delivered();
    });
  });
});

**//promise function**

function selectProduct() {
  return new Promise((resolve, reject) => {
    setTimeout(() => {
      console.log("Product selected");
      resolve();
    }, 2000);
  });
}

function addToCart() {
  return new Promise((resolve, reject) => {
    setTimeout(() => {
      console.log("Product added to cart");
      resolve();
    }, 3000);
  });
}

function payment() {
  return new Promise((resolve, reject) => {
    setTimeout(() => {
      console.log("Product payment done");
      resolve();
    }, 4000);
  });
}

function delivered() {
  return new Promise((resolve, reject) => {
    setTimeout(() => {
      console.log("Product delivered");
      resolve();
    }, 3000);
  });
}


// Promise chaining
//creating a promise is different from handling it to resolve we have .then,.catch 
selectProduct()
  .then(() => {
    return addToCart();
  })
  .then(() => {
    return payment();
  })
  .then(() => {
    return delivered();
  })
  .catch((error) => {
    console.log(error);
  });
  

Output:

Product selected
Product added to cart
Product payment done
Product delivered

//well found is for internships  purpose of internship they have many projects many clients  student can train and get employed ... noukari now ai came now internships are available startupps,apply apply apply no prepare be prepared , job based on urgency ( introduction,resume ) only you have in your hand..
