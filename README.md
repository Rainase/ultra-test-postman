# Ultra.io [![Ultra.io](https://github.com/Rainase/ultra-technical-test/blob/main/ultra-logo.png)](https://ultra.io)

## Postman API test ![workflow](https://github.com/Rainase/ultra-technical-test/actions/workflows/main.yml/badge.svg)

### In this project you'll find:

    - API tests for [Gorest](https://gorest.co.in/) endpoints using Postman and Javascript

## Usage

Downlaod the json file and import to postman and setup your api key for Gorest API.
Token can be accuired from [here](https://gorest.co.in/my-account/access-tokens)
Use postman runner to iterate trough each scenario.

## Main focus

In this test i mainly focused on "negative" 'POST' requests for creating users.

## Summary

This test sets up a request to create a new user and verifies the response body to ensure that all required fields are present, have the correct data type, and are not empty or missing. The script first retrieves a list of names from the Postman environment variables and sets the current name to either the first name in the list or a default value of "Mart" if the list is empty (when not using runner). It then sets the current gender and status to random values from predefined lists.

The script then parses the request body and response body into JSON objects and defines an object of required fields with their expected data types. It checks the request body for any missing or incorrectly formatted fields and adds them to a list of missing fields if found. If any missing fields are found, the script tests the response to ensure that it returns a status code of 422 and an array of missing fields with appropriate error messages. If no missing fields are found, the script tests the response to ensure that it returns a status code of 201 and an object with all required fields present and correctly formatted.
