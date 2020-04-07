# COVID-19 Inquire App
Use [CODVID-19 API] [(Documentation using postman)] to build mobile application that displays:
- CODVID cases per country on a MAP
- CODVID cases per country Live on a MAP (changes)
- CODVID cases per country based on a date.
- Summary of total cases for the world
- Live Summary for the World
Stretch goal:
- Display data per Province
- User can put their address and track CODVID-19 in their neighborhood (Only in countries where regional data is provided)

## Process
### Step 1: [Setup your REACT Native Environment]
- Assuming that you have [Node 12 LTS] or greater installed, you can use npm to install the Expo CLI command line utility:
```
npm install -g expo-cli
```
- After install the tools, next is to start first project
```
expo init FirstProject
```
```
cd FirstProject
```
```
npm start # you can also use: expo start
```
- Running your React Native application
Install the Expo client app on your iOS or Android phone and connect to the same wireless network as your computer. On Android, use the Expo app to scan the QR code from your terminal to open your project. On iOS, use the built-in QR code scanner of the Camera app.

### Step 2: Go through [REACT native Tutorial]
- In accordance with the ancient traditions of our people, we must first build an app that does nothing except say "Hello, world!". Here it is:
<p align="middle">
  <img src="https://github.com/BUEC500C1/codvid-app-zhangyanyu0722/blob/master/images/3.png" height="400" width="250" />
  <img src="https://github.com/BUEC500C1/codvid-app-zhangyanyu0722/blob/master/images/1.png" height="400" width="200" /> 
</p>

- Most components can be customized when they are created, with different parameters. These creation parameters are called props.
Your own components can also use props. This lets you make a single component that is used in many different places in your app, with slightly different properties in each place. Refer to props.{NAME} in your functional components or this.props.{NAME} in your class components. Here's an example:
<p align="middle">
  <img src="https://github.com/BUEC500C1/codvid-app-zhangyanyu0722/blob/master/images/Screen%20Shot%202020-04-07%20at%204.48.53%20PM.png" height="400" width="250" />
  <img src="https://github.com/BUEC500C1/codvid-app-zhangyanyu0722/blob/master/images/4.png" height="400" width="200" /> 
</p>

- In the following example we will show the same above counter example using classes.
<p align="middle">
  <img src="https://github.com/BUEC500C1/codvid-app-zhangyanyu0722/blob/master/images/Screen%20Shot%202020-04-07%20at%204.49.10%20PM.png" height="400" width="250" />
  <img src="https://github.com/BUEC500C1/codvid-app-zhangyanyu0722/blob/master/images/5.png" height="400" width="200" /> 
</p>

### Step 3: Develop use case to display a map. [GitHub location]


### Step 4: On separate branch, exercise the [CODVID-19 API] [(Documentation using postman)] and display the data in your application as text. Be fancy! Style your results.


### Step 5: Overlay the data on the maps.
 
 
[CODVID-19 API]:https://covid19api.com/
[(Documentation using postman)]:https://documenter.getpostman.com/view/10808728/SzS8rjbc?version=latest
[Setup your REACT Native Environment]:https://reactnative.dev/docs/environment-setup
[Node 12 LTS]:https://nodejs.org/en/download/
[REACT native Tutorial]:https://reactnative.dev/docs/tutorial
[GitHub location]:https://github.com/react-native-community/react-native-maps
