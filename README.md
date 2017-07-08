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
- Mobile: 95
- Desktop: 96
#### Changes made

- Removed Google fonts link and added Google fonts WebFont loader at the bottom of the body
- Added media="print" for print.css link
- Inlined the the minified CSS
- Added async tag for Google Analytics script

### Pizza Application

**Frame-rate** achieved: 60

#### Changes made

##### For scrolling
- Added will-change: transform to .mover to let the browser know that pizzas are going to transform
- In updatePositions function removed the calculation of document.body.scrollTop in for loop and added it outside the for loop.
- In updatePositions function, instead of accessing the basicLeft property of items, calucauting it in the same way it was calculated at the time of creation

##### For pizza slider
- Removed the determineDx function
- Added switch statements in changePizzaSizes function to get the newWidth variable depending on the switch size
- Calculating and storing document.querySelector(".randomPizzaContainer") in randomPizzas variable outside the for loop
- Modified the calculation of randomPizzas[i].style.width variable to get the new width of the pizzas depending on the size using newWidth variable









