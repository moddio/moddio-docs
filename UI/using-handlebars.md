# Using Handlebars in the UI

This HTML template uses Handlebars. Handlebars is a simple templating language and enables you to insert moustache expressions like `{{gameSlug}}` which get replaced with values from an input object. In the case of gameSlug, the slug of the game is returned as a string. Some expressions return full interface components like f.ex. the server list dropdown (`{{serverList}}`).  
It’s possible to apply basic logic with the use of built-in helpers like if and unless. To learn more about Handlebars you can refer to the [official documentation](https://handlebarsjs.com/guide/).  
This feature is in beta, please forward all feedback/bugs to [Bug Reports](https://www.modd.io/forum/c/bug-report/7/).  
<!-- It's also possible to make use of the Bootstrap framework that we are using. The documentation can be found  [here](https://getbootstrap.com/docs/4.1/getting-started/introduction/). -->

### Some Basic Examples of using handlebars in the UI -
### Using Variables/Components
To use variables/components we use moustache syntax `{{variable_name}}`  
Example Input:  
```
Game Slug is: {{gameSlug}}
```
Example Output: 
```
Game Slug is: two-houses (for example)
```
### if conditions
only shows contents if the condition is true  
Example Input:
```
{{#if isUserLoggedIn}}
 <h1>User is Logged In!</h1>
{{/if}}
```
Example Output:   
```
<h1>User is Logged In!</h1>
```
### unless  
inverse of if, shows content if condition is false  
Example Input:
```
{{#unless isUserLoggedIn}}
 <h1>Playing as guest!</h1>
{{/unless}}
```
Example Output:
```  
<h1>Playing as guest!</h1>
```
### ternary conditions  
additional helper to write ternary conditions.  
Example Input:  
```
class='{{ternary image 'show-image' 'hide-image'}}'
```
Example Output: 
```
class='show-image' (when image variable is 'https://some-url.xyz')
```
### each
used to iterate over an array/list  
when options = ['one', 'two', 'three']  
Example Input:
```
{{#each options}}
  <div>{{this}}</div>
{{/each}}
```
Example Output: 
```
<div>one</div>
<div>two</div>
<div>three</div>
```
