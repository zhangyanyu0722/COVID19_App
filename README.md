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
### Step 1: [Setup your REACT Native Environment] [Done]
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

### Step 2: Go through [REACT native Tutorial] [Done]
- In accordance with the ancient traditions of our people, we must first build an app that does nothing except say "Hello, world!". [See App_hello.js Here]:
<p align="middle">
  <img src="https://github.com/BUEC500C1/codvid-app-zhangyanyu0722/blob/master/images/3.png" height="400" width="250" />
  <img src="https://github.com/BUEC500C1/codvid-app-zhangyanyu0722/blob/master/images/1.png" height="400" width="200" /> 
</p>

- Most components can be customized when they are created, with different parameters. These creation parameters are called props.
Your own components can also use props. This lets you make a single component that is used in many different places in your app, with slightly different properties in each place. Refer to props.{NAME} in your functional components or this.props.{NAME} in your class components. [See App_prop.js Here]
<p align="middle">
  <img src="https://github.com/BUEC500C1/codvid-app-zhangyanyu0722/blob/master/images/Screen%20Shot%202020-04-07%20at%204.48.53%20PM.png" height="400" width="250" />
  <img src="https://github.com/BUEC500C1/codvid-app-zhangyanyu0722/blob/master/images/4.png" height="400" width="200" /> 
</p>

- In the following example we will show the same above counter example using classes.[See App_class.js Here]
<p align="middle">
  <img src="https://github.com/BUEC500C1/codvid-app-zhangyanyu0722/blob/master/images/Screen%20Shot%202020-04-07%20at%204.49.10%20PM.png" height="400" width="250" />
  <img src="https://github.com/BUEC500C1/codvid-app-zhangyanyu0722/blob/master/images/5.png" height="400" width="200" /> 
</p>

### Step 3: Develop use case to display a map. [GitHub location] [Done]
#### Install and set up React Native application
- If you haven’t installed the React Native command line interface, run: ```npm install -g react-native-cli``` 
- Now you can create your project, simply using ```react-native init ReactNativeMaps```
- After installing, Now you can try to run your app, ```react-native run-ios```
#### Add and Link react-native-maps package
- Now let’s install react-native-map: ```npm install --save react-native-maps```
- After installing the package you should link it to your native apps: ```react-native link react-native-maps```.
#### Set up Apple Maps (iOS):
- It will be easier if we set them up separately by platform, so let’s first do it on iOS. Before integrating Google Maps, we will check if Apple Maps works correctly. Add the following code to your current rendering component where you want to render your MapView.
<p align="middle">
  <img src="https://github.com/BUEC500C1/codvid-app-zhangyanyu0722/blob/master/images/apple1.png" height="300" width="200" />
  <img src="https://github.com/BUEC500C1/codvid-app-zhangyanyu0722/blob/master/images/apple.png" height="400" width="200" /> 
</p>
- So, as you can see, by default Apple Maps is already working. More than that, if you linked everything correctly and enabled the user location, it’s actually done a lot of things for us (the user permission for the location with a default message). If you came from native iOS development, then you probably know what is an info.plist file.

#### Install Cocoapods and ‘GoogleMaps’ package (iOS)
- Run ```sudo gem install cocoapods``` to install the Cocoapods.
- Navigate to your **iOS** folder in React Native app and run ```pod install```
- Then we need to navigate to **AirGoogleMaps** folder from **node_modules** and add all to the **ios**
- After that, Navigate to your **iOS/ReactNativeMaps/AppDelegate.m** file and add the code below into it.
<p align="middle">
  <img src="https://github.com/BUEC500C1/codvid-app-zhangyanyu0722/blob/master/images/Screen%20Shot%202020-04-10%20at%208.50.38%20PM.png" width="600">
</p>

***Use your own google_api_key here, for more detail, visit : [google api setup]***

<p align="middle">
  <img src="https://github.com/BUEC500C1/codvid-app-zhangyanyu0722/blob/master/images/Screen%20Shot%202020-04-10%20at%208.51.02%20PM.png" width="600"> 
</p>

- Now run your iOS app. And you will get Google Maps.

<p align="middle">
  <img src="https://github.com/BUEC500C1/codvid-app-zhangyanyu0722/blob/master/images/google1.png" height="300" width="200" />
  <img src="https://github.com/BUEC500C1/codvid-app-zhangyanyu0722/blob/master/images/google.png" height="400" width="200" /> 
</p>


### Step 4: On separate branch, exercise the [CODVID-19 API] [(Documentation using postman)] and display the data in your application as text. Be fancy! Style your results. [Done]
- In order to get the increasement informantion, I use the [CODVID-19 API] to get the confirmed number by states.
```
curl --location --request GET https://api.covid19api.com/live/country/united-states/status/confirmed/date/2020-04-10T20:00:00Z
```
<p align="middle">
  <img src="https://github.com/BUEC500C1/codvid-app-zhangyanyu0722/blob/master/images/postman.png" height="300" width="500" > 
</p>

- Or I can get all of the cases in one day in united states

```
curl --location --request GET https://api.covid19api.com/dayone/country/united-states/status/confirmed
```

<p align="middle">
  <img src="https://github.com/BUEC500C1/codvid-app-zhangyanyu0722/blob/master/images/cases.png" height="300" width="500" > 
</p>

### Step 5: Overlay the data on the maps. [Done]
- Click the right bottom button to show the cases near your current location. And you can see the result as following
<p align="middle">
  <img src="https://github.com/BUEC500C1/codvid-app-zhangyanyu0722/blob/master/images/result.png" height="400" width="200">
  <img src="https://github.com/BUEC500C1/codvid-app-zhangyanyu0722/blob/master/images/result2.png" height="400" width="200"> 
</p>
 
[CODVID-19 API]:https://covid19api.com/
[(Documentation using postman)]:https://documenter.getpostman.com/view/10808728/SzS8rjbc?version=latest
[Setup your REACT Native Environment]:https://reactnative.dev/docs/environment-setup
[Node 12 LTS]:https://nodejs.org/en/download/
[REACT native Tutorial]:https://reactnative.dev/docs/tutorial
[GitHub location]:https://github.com/react-native-community/react-native-maps
[See App_hello.js Here]:https://github.com/BUEC500C1/codvid-app-zhangyanyu0722/blob/master/App_hello.js
[See App_prop.js Here]:https://github.com/BUEC500C1/codvid-app-zhangyanyu0722/blob/master/App_prop.js
[See App_class.js Here]:https://github.com/BUEC500C1/codvid-app-zhangyanyu0722/blob/master/App_class.js
[google api setup]:https://developers.google.com/maps/documentation/ios-sdk/get-api-key

