# Web app requirement

A web application connects to a server application. On login, the server app creates a session and sends the session info to the web app. The session is created with a maxInactiveInterval value. With each call from web app to server the lastAccessedTime value of the session is updated. When the value of lastAccessedTime reaches maxInactiveInterval, the server kills the session and logs of the user in the web application. 

The web application should implement a mechanism so that the server keeps the session alive as long as the user is active on the web application even if not making any calls to the server. 

The web application is built in React. Put console log statements instead of actually making a call to a server. 

### Task 1

Implement react-idle-timer in the web application. This component will set a global variable called isActive to true. When the user is inactive, isActive is set to false. When the user becomes active again, isActive is set to true. 

### Task 2

Create a timer that will run every 60 seconds. If isActive is true then make a call to the server. If isActive is false, do nothing.