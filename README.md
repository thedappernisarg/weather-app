# weather-app
Build a simple Weather App with Node.js 

**Pre Project Setup**
1. Open a account in <a href="https://openweathermap.org/api">OpenWeatherMap.org</a> account. it would take 20 seconds for signup.
2. Download <a href="https://nodejs.org/en/">Node.js</a>

**Projet Setup**
1. Create a directory called weather-app.
2. Open up your console, navigate to our new directory and run npm init.
3. Fill out the required information to initialize our project.
4. Within our weather-app directory, create a file named ```index.js``` — this file will house the code for our application.

**Creating a Server (With Express JS)**

To use express, install it in the console:
``` npm install --save express ```

**Setting up the index view**
Instead of responding with text when someone visits our root route, we’d like to respond with an HTML file. For this, we’ll be using EJS (Embedded JavaScript). 

( EJS is a templating language. A template engine enables you to use static template files in your application. At runtime, the template engine replaces variables in a template file with actual values, and transforms the template into an HTML file sent to the client. This approach makes it easier to design an HTML page.)

**body-parser middleware** 
body-parser allows us to make use of the key-value pairs stored on the req-body object. In this case, we’ll be able to access the city name the user typed in on the client side. 
``` npm install body-parser --save ```


To make our API call, we’ll be using a popular npm module called request. 
We just need to pass in our target url, and request returns a callback function
 ``` npm install request --save ```

By reading the OpenWeatherMap Documentation, we are able to determine that this is url. we should make our requests to: http://api.openweathermap.org/data/2.5/weather The URL also has two required query parameters. Query parameters are key/value pairs that allow us to pass in data to a URL.

If you use Celsius you’d add: ``` units=metric ``` and If you use Fahrenheit you’d use ``` units=imperial ```

**Yargs** is a pirate themed interactive command line interface tool. Or more simply put, it allows us to define variables from the command line.

**Notes:**

 The app.get('/'... means we are specifically focusing on the root URL (/). If we visit the root URL, Express will respond with “Hello World!”.

``` app.set('view engine', 'ejs')
app.get('/', function(req, res){ 
	//res.send('Hello World');
	//res.render will render our view, 
    res.render('index');
}); 
```

The app.listen(... shows we are creating a server that is listening on port 3000 for connections.

``` 
app.listen(3000, function(){
   console.log('Example app listening on port 3000!');
}); 
```
