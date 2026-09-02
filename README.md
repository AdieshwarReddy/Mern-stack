# Mern-stack

>Js 
// call back functions ,promises (.then  and .catch ,.asynch)
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
