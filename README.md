<br>

# CZC - Selenium Website Testing | Semester Project


> **Author** | Ľuboslav Motošický, @lubiku35
>
> **Subject** | Software Testing
>
> **Project Name** | CZC - Selenium Website Testing 

<br>

# Project Introduction

Welcome to my Selenium Website Testing project! In this endeavor, I have undertaken the task of ensuring the quality and reliability of the website https://www.czc.cz/. I have chosen this website as the target for my testing efforts due to its popularity and the diverse functionalities it offers.

Throughout this project, I have conducted a comprehensive range of tests, starting from basic ones like accepting cookies and verifying the page title, and progressing towards more sophisticated scenarios such as user registration, login functionality, and adding products to the cart. By covering various aspects of the website, I aim to identify and address any potential issues, ensuring a seamless and satisfying user experience.

<br>

# Navigation

- [Selected Technologies](#selected-technologies)
- [Application Functionalities](#application-functionalities)  
    - [Product Catalog](#product-catalog)  
    - [Registration and Login](#registration-and-login)  
    - [Favorites](#favorites)  
    - [Wishlist](#wishlist)  
    - [Shopping Cart and Checkout](#shopping-cart-and-checkout)  
    - [Discussions and Reviews](#discussions-and-reviews)
- [Tests Prioritization](#tests-prioritization)
- [Tests Overview](#tests-overview)  
    - [Demo Tests](#demo-tests)
        - [Accept Cookies Test](#accept-cookies-test)
        - [Browse Through Website Test](#browse-through-website-test)
        - [Create New Account Test](#create-new-account-test)
        - [Login Test](#login-test)
        - [Page Title Test](#page-title-test)
        - [Search Test](#search-test)
        - [Parameterized Search Test](#parameterized-search-test)
        - [Shopping Cart Test](#shopping-cart-test)
        - [Subscribe to Action Offers Test](#subscribe-to-action-offers-test)
    - [Main Test](#main-test)

<br>

# Selected Technologies

> Java, Selenium, Selenide, Allure, Allure JUnit, Allure Selenide, WebDriverManager, JUnit Jupiter API and JUnit Jupiter Engine, SLF4J Simple

- **Selenium**: A popular open-source framework for automating web browsers.
- **Selenide**: A wrapper framework built on top of Selenium that provides a more concise and expressive syntax for writing UI tests.
- **Allure**: A test reporting framework that generates visually appealing and informative reports.
- **Allure JUnit 5**: The Allure integration for JUnit 5, which allows seamless integration with Allure reporting in JUnit 5 tests.
- **Allure Selenide**: An extension for Allure that captures Selenide-specific logs and integrates them into the Allure reports.
- **WebDriverManager**: A library that automates the management of WebDriver binaries, making it easier to set up and use different web browsers for testing.
- **JUnit Jupiter API and JUnit Jupiter Engine**: The JUnit 5 framework for writing and executing tests.
- **SLF4J Simple**: A simple implementation of the Simple Logging Facade for Java (SLF4J) API, which provides basic logging functionality for tests.

To accomplish my testing goals, I have utilized the Selenium framework in combination with the powerful Selenide library. Selenide provides a user-friendly and concise syntax for writing automated tests, allowing me to efficiently interact with web elements, simulate user actions, and validate the expected behaviors of the website.

As part of my testing strategy, I have incorporated the Allure reporting framework, which generates comprehensive and visually appealing reports. With Allure, I can present my test results in a professional manner, providing detailed insights into the test execution, including step-by-step logs, screenshots, and overall test outcomes. This enhances my ability to track and analyze test failures, making it easier to identify and resolve any potential issues.

<br>

# Application Functionalities

CZC web application is an e-commerce platform specializing in the sale of gaming, electronic, and various other accessories. The primary purpose of this application is to provide users with a seamless and enjoyable shopping experience for their desired products.

## Product Catalog

The application provides a comprehensive product catalog featuring gaming, electronic, and accessory items. Users can browse through different categories, view detailed product information, and add items to their favorites.

## Registration and Login

Users can create an account by registering with their relevant information, including name, email address, and password. Once registered, they can securely log in to their accounts to access personalized features and preferences.

## Favorites

The favorites functionality allows users to mark specific products as their favorites for quick access and future reference. By adding items to their favorites list, users can easily keep track of products they are interested in or plan to purchase later.

## Wishlist

In addition to favorites, the application also offers a wishlist feature. Users can add products to their wishlist to create a curated collection of items they aspire to own. The wishlist provides a convenient way to organize and save desired products.

## Shopping Cart and Checkout

Users can add products to their shopping cart and proceed to checkout when ready to make a purchase. The application offers a streamlined and secure checkout process, allowing users to review their cart, apply discounts or promo codes, select shipping options, and complete the transaction.

## Discussions and Reviews

The application includes a discussion platform where users can engage with others, ask questions, share experiences, and provide feedback or reviews on products. This feature promotes user interaction and helps users make informed purchase decisions.

<br>

# Project Tests Prioritization

When comes to prioritizing tests for the web application, it's essential to focus on critical areas and features that have a significant impact on the overall functionality and user experience. Here you can find my suggested prioritization for this project:

| **Priority**    | **Test Area**                     |
|-----------------|-----------------------------------|
| Low             | `Accept Cookies`                  |
| Low             | `Login and Registration`          |
| Low             | `HomePage and Navigation`         |
| Medium          | `Product Catalog`                 |
| Medium          | `Favorites and Wishlist`          |
| High            | `Add to Cart`                     |
| High            | `Checkout Process`                |

<br>

# Tests Overview

## Demo Tests

### Accept Cookies Test

This test case validates the functionality of accepting cookies on the website. It ensures that the user can successfully click on the "Accept Cookies" button to acknowledge and accept the use of cookies on the website.

1. Navigate to the website URL.
2. Click on the "Accept Cookies" button.


### Browse Through Website Test

This test case verifies the functionality of browsing through various elements on the website. It uses parameterized testing to iterate over a set of elements and clicks on each element to navigate to the corresponding page.

1. Navigate to the website URL.
2. Accept cookies by clicking on the "Accept Cookies" button.
3. Click on the main page link to ensure you start from the homepage.
4. **Parameterized Test**: Iterate over a stream of elements.
5. For each element, click on it to navigate to the corresponding page.
6. After each iteration, return to the main page to reset the state for the next iteration.

### Create New Account Test

This test case verifies the functionality of creating a new account on the website.

1. Navigate to the website URL.
2. Accept cookies by clicking on the "Accept Cookies" button.
3. Find and Click on the "Create Account" button to navigate to the registration form.
4. Verify that the registration heading contains the expected text.
5. Verify the visibility of all necessary components on the registration form.
6. Verify if the "Register" button is visible.

### Login Test

This test case verifies the functionality of the login process on the website.

1. Navigate to the website URL.
2. Accept cookies by clicking on the "Accept Cookies" button.
3. Click on the "Login" button to navigate to the login form.
4. Verify the visibility of the login input fields (username and password).
5. Check if the labels for the username and password inputs are visible.
6. Verify the visibility of the login button and the button to accept the login terms.

### Page Title Test

This test case checks the title of the webpage and verifies that it matches the expected title.

1. Navigate to the website URL.
2. Retrieve the actual page title using Selenide's title() method.
3. Compare the actual page title with the expected page title.
4. Assert that the actual page title is equal to the expected page title.

### Search Test

This test case searches for a specific value (in my case, "Iphone") on the website and verifies the search results. 

1. Accept cookies if necessary by clicking on the accept cookies button.
2. Locate the search input element and set its value to the searched value ("Iphone").
3. Click on the search button.
4. Set the timeout for element search to 6000 milliseconds.
5. Verify that the search heading is visible and contains the searched value.
6. Retrieve the first three search results and store them in a list of SelenideElements.
7. Iterate over the first three search results and verify that each result has a button to add the item to the shopping cart.


### Parameterized Search Test

This test case performs a search on the website using different search values. It uses parameterized testing, where the search values are provided through a CSV source.

1. Set up the test environment by opening the website and accepting cookies.
2. Locate the search input element and set its value to the current search value.
3. Click on the search button.
4. Set the timeout for element search to 6000 milliseconds.
5. Verify that the search heading is visible and contains the current search value.
6. Retrieve the first three search results and store them in a list of SelenideElements.
7. Iterate over the first three search results and verify that each result has a button to add the item to the shopping cart.

### Shopping Cart Test

This test ensures that the shopping cart functionality is working correctly by adding items to the cart, navigating to the cart page, and performing necessary actions.

1. Set up the test environment by opening the website, accepting cookies, and locating the shopping cart button.
2. Click on the shopping cart button.
3. Verify that the empty shopping cart heading is visible.
4. Click on the "Back to Shop" button to return to the main shop page.
5. Locate an element selected for user in the carousel and click on its button.
6. Click on the shopping cart button again.
7. Verify that the "Proceed to Checkout" button is visible.

### Subscribe to Action Offers Test

The SubscribeToActionOffersTest is a parameterized test case that verifies the functionality of subscribing to action offers on the website.

1. Set up the test environment by opening the website, accepting cookies, and locating the subscribe input field and button.
2. For each parameterized input value (email address) in the CSV source, perform the following steps:
- Set the value of the subscribe input field to the current email value.
- Click on the subscribe button.
3. After each test iteration, click on the main page link to navigate back to the main page.

## Main Test

The MainTest represents a comprehensive test scenario that simulates a user's interaction with the website. Here's a description of the test scenario:

> This test scenario simulates the user's journey on the website. 

The user performs the following steps:

1. **Accept Cookies** :
- The user accepts the cookies by clicking on the "Accept" button.

2. **Navigate to Create New Account** :

- The user clicks on the "Login" button to initiate the registration process.
- The user verifies that the registration heading contains the expected text.
- The user clicks on the registration button to navigate to the registration form.
- The user verifies the visibility of all necessary components in the registration form.

3. **Create New Account** :

- The user fills in the registration form with the provided user details.
- The user clicks on the "Register" button to create a new account.
- The user clicks on the main page link to navigate back to the main page.

4. **Login to Already Created Account** :

- The user clicks on the "Login" button.
- The user enters the login credentials (username and password) for the already created account.
- The user clicks on the "Accept" button to log in.
- The user clicks on the main page link to navigate back to the main page.

5. **Preview My Current Orders** :

- The user clicks on the user's profile link.
- The user triggers the menu by moving the mouse cursor over the user's profile menu.
- The user clicks on the "My Orders" link from the menu.
- The user checks that "My Orders" section is empty and clicks on the main page link to navigate back to the main page.

6. **Preview Empty Shopping Cart** :

- The user clicks on the shopping cart button.
- The user verifies the visibility of the empty shopping cart heading.
- The user clicks on the "Back to Shop" button to navigate back to the main page.

7. **Make Random Choice from Selected Items and Add It to the Shopping Cart** :

- The user makes a random choice from the selected items carousel and adds it to the shopping cart.
- The user clicks on the shopping cart button to view the shopping cart.

8. **Navigate Through the Shopping Cart Menu** :

- The user proceeds with the order by clicking on the confirmation buttons.
- The user clicks on the "Close the Order" button and navigates back to the shopping cart.
- The user removes the current item from the shopping cart.
- The user clicks on the "Navigate Back to the Shop" button to return to the main page.

9. `Make Random Choice from Selected Items and Add It to the Wishlist`:

- The user makes a random choice from the selected items carousel and adds it to the wishlist.
- The user clicks on the main page link to navigate back to the main page.

10. **Search Products** :

- The user performs a search for various products using the provided search values.
- The user verifies the search results and the visibility of the "Add to Cart" buttons for the first three results.
- The user clicks on the main page link to navigate back to the main page.

> This comprehensive test scenario covers various user actions on the website, including registration, login, cart management, wishlist management, and product search.
