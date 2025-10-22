# Django - Intro 1: Request and Response

## Objectives

By the end of this assignment you should be able to:

- Grasp how HTTP requests and responses work.
- Create basic views that handle requests and return responses.
- Explore how to return different response types.


## Assignment

In the provided [functions-over-http](./exercises/functions_over_http) project's `app` app, implement the following view and path pairs. Test cases have been provided to help you check your work. Also type annotations are required.

1. [ ] **Hello World** Your app should respond with `Hello World!` when a request is made to `/hello`. For example, a request to `/hello` should respond with `Hello World!`.
2. [ ] **Hey You:** Your app should respond with `Hey, <name>!` when a request is made to `/hey/<name>`. For example, a request to `/hey/bcca` should respond with `Hey, BCCA!`.
3. [ ] **How Old:** Your app should respond with a user's age in some provided end year when a request is made to `/age-in/<end>/<birthyear>`. For example `/age-in/2050/2000` should respond with `50`. Your path should appropriately indicate that the `end` and `birthyear` path arguments are integers.


### How to run test cases.
Mac: python3 manage.py test
Windows: python manage.py test


### Common Misconceptions/Errors to Watch Out For

- Neglecting URL Configuration: Failing to properly configure urls.py or forgetting to include URL patterns. This can lead to 404 errors and make views inaccessible.
- Overcomplicating Function-Based Views: Using overly complex logic in function-based views instead of keeping them simple and focused. This reduces readability and maintainability, making it harder to debug.
- Not Handling Different HTTP Methods: Assuming a view will only handle one type of request (e.g., GET) and not implementing checks for POST or other methods. This can result in incorrect handling of form submissions or API requests.
- Ignoring Form Validation Errors: Not properly validating forms and failing to display error messages to users. Users may be confused by silent failures or not understand what went wrong.
- Returning Data Without Context: Rendering templates without passing necessary context data. This can lead to incomplete or broken pages due to missing information.
- Using Hardcoded URLs: Hardcoding URLs instead of using the reverse() function or the {% url %} template tag. This makes it difficult to change URL patterns in the future, leading to broken links.
- Not Using get_object_or_404(): Failing to use get_object_or_404() when retrieving objects by ID. This can result in unhandled exceptions if an object does not exist, leading to 500 errors instead of a user-friendly 404 page.
- Poorly Managing Redirects: Not using appropriate redirect responses after form submissions or actions. This can lead to duplicate submissions if users refresh the page.
- Mixing Business Logic with View Logic: Placing too much business logic directly in views instead of separating it into models or utility functions. This makes views harder to test and maintain.
- Neglecting Testing for Views: Skipping unit tests for views, assuming they work fine without testing.This can lead to unnoticed bugs and regressions in functionality.

