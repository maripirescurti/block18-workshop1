# WORKSHOP I
Goal: Write test specifications for a series of prompts

## Prompts:

For each prompt below:
- Read the prompt.
- Identify the expectations.
- Write specifications in pseudocode/plain English for all the tests that would be useful for that prompt.
  - Try to take any "edge cases", or unexpected circumstances, into account, and write test specs for them.
  - Try not to write extraneous tests!

  ## Unit Tests:

  1. A function called "multiplication" that returns the product of the two input number.

    ### Tests:

      Test 2 positive numbers:  
      Expect [multiplication(3, 5)] to be a number

      Test 2 positive numbers: 
      Expect [multiplication(3, 5)] to be equal to 15
      
      Test 2 negative numbers: 
      Expect [multiplication(-3, -5)] to be a positive number

      Test 2 negative numbers:
      Expect [multiplication(-3, -5)] to be equal to 15

      Test one negative and one positive number:
      Expect [multiplication(-3, 5)] to be a negative number

      Test one negative and one positive number:
      Expect [multiplication(-3, 5)] to be equal to -15

      Test one string and one number:
      Expect [multiplication('a', 3)] to be an error

      Test two strings:
      Expect [multiplication('a', 'b')] to be an error

      Test 0 and number:
      Expect [multiplication(0, 5)] to be equal to 0

      Test decimal numbers:
      Expect [multiplication(3.5, 5.5)] to be equal to 19.25


  2. A function called "contactOdds" takes two arrays of integers as arguments. It should return a single array that only contains the odd numbers, in ascending order, from both the arrays.

    Tests:

      Test two arrays of numbers containing odds and evens, and both arrays have odds:
      Expect [concatOdds([1, 2, 3], [4, 5, 6])] to result in [1, 3, 5]

      Test two arrays of numbers containing odds and evens, and only one array has odds:
      Expect [concatOdds([1, 3, 5], [2, 4, 6])] to result in [1, 3, 5]

      Test two arrays of numbers containing just odd numbers:
      Expect [concatOdds([1, 3, 5], [7, 9, 11])] to result in [1, 3, 5, 7, 9, 11]

      Test two arrays of numbers containing just even numbers:
      Expect [concatOdds([2, 4, 6], [8, 10 ,12])] to result in [] = empty array

      Test one array with odd numbers and one empty array:
      Expect [concatOdds([1, 2, 3, 4, 5], [])] to result in [1, 3, 5]

      Test one array without odd numbers and one empty array:
      Expect [concatOdds([2, 4, 6, 8], [])] to result in [] = empty array

      Test two empty arrays:
      Expect [concatOdds([], [])] to result in [] = empty array

      Test two arrays of numbers containing negative numbers:
      Expect [concatOdds([-1, 2, 3], [-4, 5, 6])] to result in [-1, 3, 5]

      Test two arrays with numbers and strings:
      Expect [concatOdds([-1, 2, 'apple', 3], [-4, 5, 'b', 6])] to result in [-1, 3, 5]

      Test two arrays with just strings in both of them:
      Expect [concatOdds(['a', 'b', 'c'], ['apples', 'bananas', 'oranges'])] to result in [] = empty array

      Test two arrays with decimal numbers:
      Expect [concatOdds([1.1, 2.3, 3.4], [5.66, 6.73, 8.8])] to result in [1.1, 2.3, 6.73]

      Test two arrays with both decimal numbers and whole numbers:
      Expect [concatOdds([1.1, 2, 3.4], [5, 6.73, 8])] to result in [1.1, 5, 6.73]

  ## Functional Tests:

    1. A shopping cart checkout feature that allows a user to check out as a guest (without an account), or as a logged-in user. They should be allowed to do either, but should be asked if they want to create an account or log in if they check out as a guest.

      When a user clicks "Log-in" without filling in any information, they should be shown an error and prompted to log in, sign up, or continue as guest

      When a user clicks "Log-in" but has filled in incorrect information, they should be shown an error and prompted to sign up or continue as guest

      When a user clicks "Log-in" and has filled in their information correctly, they should be taken to the cart checkout page, while logged in to their account, where they will see the cart and payment information which should be already filled in with previously used information to be reviewed before finalizing the purchase (stored credit card, stored address, any coupons or discounts). 

      When a user clicks "Log-in" and has filled in their information correctly, but has not put anything in their cart, they should be taken to the main shopping page where they can browse for different products to put into their carts. 

      When a user clicks "Check out as guest", with items in their cart, they should be prompted to provide their shipping and billing information, and then the user will be asked if they want to create an account for future purchases, if they want to log in, or just checkout as guest. 
        - If they continue to checkout as guest they will proceed with finalizing the purchase
        - If they click "log-in" they will be redirected to a page where theire billing and shipping information is stored, and they can review the cart and checkout with pre-filled information
        - If they click "sign-up", the user will be prompted to create a username and password, and after they confirm, they will be redirected to their cart, where the shipping and billing information they input before will be stored and they can finalize their purchase.

      When a user clicks "Check out as a guest", with no items in their cart, they should be asked if they want to be redirected to the shopping page to put items in their cart. 

      

      





    
  

  



