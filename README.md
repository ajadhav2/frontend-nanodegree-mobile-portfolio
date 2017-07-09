# Website Optimization

This file contains **instructions** on how to run the application and outlines the optimizations that the I made in index.html and views/js/main.js for pizza.html.

## Run the Application
To run the application perform following steps
- Unzip frontend-nanodegree-mobile-portfolio.zip file
- Go to frontend-nanodegree-mobile-portfolio folder
##### To Run the Portfolio Application
  - Open index.html file in the browser
##### To Run the Pizza Application
  - Go to views folder in frontend-nanodegree-mobile-portfolio folder
  - Open pizza.html file in the browser

## Optimization Made

### Portfolio Application

**PageSpeed** achieved
-  Mobile: 95
- Desktop: 96
#### Changes made

- Removed Google fonts link and added Google fonts WebFont loader at the bottom of the body
- Added media="print" for print.css link
- Inlined the minified CSS
- Added async tag for Google Analytics script
- Compressed the profilepic.jpg and pizzeria.jpg images

### Pizza Application

**Frame-rate** achieved: 60

#### Changes made

##### For scrolling
- Added will-change: transform to .mover to let the browser know that pizzas are going to transform
- In updatePositions function removed the calculation of document.body.scrollTop in for loop and added it outside the for the loop.
- In updatePositions function, instead of accessing the basicLeft property of items, calculating it in the same way it was calculated at the time of creation

##### For pizza slider
- Removed the determineDx function
- Added switch statements in changePizzaSizes function to get the newWidth variable depending on the switch size
- Calculating and storing document.querySelector(".randomPizzaContainer") in randomPizzas variable outside the for loop
- Modified the calculation of randomPizzas[i].style.width variable to get the new width of the pizzas depending on the size using newWidth variable

###### Changes in the code(views/main.js)
- used document.getElementById istead of document.querySelector for pizzaSize element
- used document.getElementsByClassName() Web API instead of document.querySelectorAll for class randomPizzaContainer and for class mover
- storing the randomPizzas array length in len variable
- declaring pizzasDiv variable outside for loop
- changed the number of sliding pizzas from 200 to 24
- declaring pizza variable elem outside the for loop
- Get the element with the id movingPizzas1 and store it in movingPizzas variable
- Append elem to movingPizzas

###### Changes in the code(views/css/style.css)
- added transform: translateZ(0) and backface-visibility: hidden to mover class






























