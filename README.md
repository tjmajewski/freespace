# freespace

const Kelvin = 50; // Kelvin will always equal 293
const Celsius = Kelvin-273; // celsius will always be 273 less than Kelvin
let Fahrenheit = Celsius*(9/5)+32; // calculating fahrenheit from celsius
Fahrenheit = Math.floor(Fahrenheit); // puts Fahrenheit as whole number
let Newton = Celsius * (33/100); // convert Celsius to Newton
Newton = Math.floor(Newton);
console.log(`The temperature is ${Fahrenheit} degrees Fahrenheit.`);
console.log(`The temperature is ${Newton} degrees Newton`);
