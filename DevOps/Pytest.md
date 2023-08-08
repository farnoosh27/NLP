# Testing 

unittest is a built-in testing framework in the Python Standard Library. It follows the xUnit style and provides a way to create tests by writing test classes that inherit from unittest.TestCase

## Level of testing
- **Unit Testing**  
  Testing at the function level.

- **Component Testing**  
  Testing is at the library and compiled binary level.

- **System Testing**  
  Tests and external interfaces of a system which is a collection of sub-systems.

- **Performance Testing**  
  Evaluating the performance of the software under different conditions.


  Testing is done at sub-system and system levels to verify timing and resource usage and acceptable.
## Pytest
Pytest is a widely used Python testing framework, offering a user-friendly and concise syntax for writing test cases. 
It provides powerful built-in assertions, automatic test discovery, and support for fixtures to set up resources. Pytest is highly extensible through plugins and allows parameterized testing. Its simplicity and flexibility have made it a popular choice in the Python community.
 ## Testing a simple function
Step 1: Install pytest
Make sure you have Python installed on your system. You can download Python from the official website (https://www.python.org/downloads/).

Next, you can install pytest using pip. Open your terminal or command prompt and run the following command:

```
pip install pytest
```
Step 2: Write the super simple function
Let's create a simple function in Python that we'll use for testing. For this example, let's create a function that adds two numbers:

# save this code in a file named simple_function.py
```
def add_numbers(a, b):
    return a + b
```
Step 3: Write the test for the function
Now, we'll write a test for the add_numbers function using pytest. Create a new file called test_simple_function.py and save it in the same directory as simple_function.py.


# save this code in a file named test_simple_function.py
```
from simple_function import add_numbers

def test_add_numbers():
    result = add_numbers(2, 3)
    assert result == 5

    result = add_numbers(-1, 1)
    assert result == 0

    result = add_numbers(0, 0)
    assert result == 0
```
In this test, we're using the assert statement to check whether the actual result of the add_numbers function matches the expected result.

Step 4: Run pytest
Now that we have our function and test written, it's time to run pytest. Open your terminal or command prompt and navigate to the directory where you saved the simple_function.py and test_simple_function.py files.

Run the following command:
```
pytest
```

## What are fixtures within Pytest?
 A pytest fixture is like a helper function that prepares something needed for your tests. It can be data, resources, or setup. You define a fixture using @pytest.fixture above a function. Inside that function, you set up what's needed and use yield to provide it to your test functions
