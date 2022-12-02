
# Ask Yoda
"You must unlearn what you have learned."
"The greatest teacher, failure is."
## 
![Joda](https://bbts1.azureedge.net/images/p/full/2020/01/c58f6f4d-8622-44c3-b68d-e464ba045503.jpg)
<img src="https://github.com/favicon.ico" width="48">
## FAQ

#### Question 1: Can I modify the DSK directory structures of my project?

No, you must left the original project structures and put your code in the /src directory for example.

#### Question 2: Could I have parameters not referenced in aws template?

No, you must clean parameters that you don't use

#### Question 3: Can I hardcode URLs, user, passwords or tokens?

No, never do that. You could use properties files o .env files or secrets to put confidencial information.

#### Question 4: Could I have BL and Service implementations without unit tests in my code?
No, you mustn't. You must have 2 escenarios covered at minimum peer function. 

#### Question 5: What I need to verify in a code review?
The basic review could cover the followings:
1. Follow Java code conventions: For instance, all package names in Java are written in lowercase, constants in all caps, variable names in CamelCase, etc.
2. Beware of the NullPointerException: When writing new methods, try to avoid returning nulls if possible. It could lead to null pointer exceptions.
3. Handle exceptions with care: While catching exceptions, if you have multiple catch blocks, ensure that the sequence of catch blocks is most specific to least.
4. Every new funtionality need to be tested: Testing the functionality and output of the new code sections can drastically reduce review time later.
5. Ensure pull requests are small and with a singular purpose

#### Question 4: How to avoid pipeline errors?
You could use gradlew commands before push your code e.g. gradlew test, gradlew build, etc. Other common error is the dockerfile fail, to test it you can use: docker build -f "path/to/file" -t "example" .

