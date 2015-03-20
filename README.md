# ngStub

Load dynamically stubs to simulate http request response in an angular enviroment

#Motivation 

In angular development we must make request to a server a lot of times to support dinamycs contents, but in the development fase the server side can be in development (Only with the document of future implementation) or constant changing (new features), and if you want to test some logic you need to wait for the server response or run your custom server. In my case, this is to complicate when you only want test your directives or application flows.

Another approach is use the same stubs in development in the test, not mock the application with the expexted response.

#Proposition

One service

```javascript
angular.module('app')
	.config(function($ngStub){
		$ngStub.loadStub('url_to_stub');
		$ngStub.activateStub();
	})
```