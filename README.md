# Fetch Fake Store API

Welcome to my project! This project demonstrates fetching and displaying data from the Fake Store API on a simple webpage.

## Table of Contents
- [Overview](#overview)
- [Technologies Used](#technologies-used)
- [Features](#features)
- [Demo](#demo)
- [Getting Started](#getting-started)
- [How to Use](#how-to-use)
- [Code Snippet](#code-snippet)
- [Contributing](#contributing)
- [License](#license)

## Overview
This project is a part of my journey in web development, focusing on API integration and dynamic content rendering. It fetches product data from the Fake Store API and displays it in an organized manner on the webpage.

## Technologies Used
- HTML
- CSS
- JavaScript

## Features
- Utilizes Flexbox for responsive product card layout
- Dynamically fetches and displays product information from the Fake Store API

## Demo
![image](https://github.com/Abhi865625/Fake-Store-Api/assets/93569162/16920b24-6484-427d-947c-bfc264c9583b)


## Getting Started
To get a local copy up and running, follow these simple steps:

1. Clone the repository
   ```bash
   git clone https://github.com/your-username/your-repo.git

** Open index.html in your browser **

## How to Use
Once the webpage is open, you'll see a collection of product cards fetched from the Fake Store API. Each card includes details like title, image, description, category, and price.

## Code Snippet
// Fetch data from the Fake Store API
fetch("https://fakestoreapi.com/products")
  .then((data) => data.json())
  .then((completedata) => {
    let data1 = "";
    completedata.map((values) => {
      data1 += `<div class="card">
        <h1 class="title">${values.title}</h1>
        <img src="${values.image}" alt="img" class="images" />
        <p>${values.description}</p>
        <p class="category">${values.category}</p>
        <p class="price">$${values.price}</p>
      </div>`;
    });
    document.getElementById("cards").innerHTML = data1;
  })
  .catch((err) => {
    console.log(err);
  });

## Contributing
Contributions are welcome! Feel free to open an issue or submit a pull request.
