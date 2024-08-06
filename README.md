# weatherforcast -Weather app using React
<h1>Enter a city and know the temprature</h1><br>

![alt text](https://github.com/pybraham/weatherforcast/blob/main/munweather.png?raw=true) <br>
To get such a result for entering any city, I use react. <br>

**react**
<br>**Setting up a React Environment**<br>
If you have npx and Node.js installed, you can create a React application by using create-react-app
**npx create-react-app my-app**<br>
Run this command to move to the my-react-app directory:
**cd my-react-app** <br>
Run this command to run the React application my-react-app:
**npm start** <br>
A new browser window will pop up with your newly created React App! If not, open your browser and type localhost:3000 in the address bar.
<br>
**Create folders** <br>
1.Weather/src<br>
2.src/components<br>
3.src/Images<br>
<br>
The first Weather/src will have the root directory including App.js and the JSON package.<br>
The second src/Components has functions of  MainweatherWindow.js,Weatherbox.js.<br>
The third folder has just sample pics of a sun, cloudy,rainy, pngs<br>
<br>
**use your IDE such as Visual Studio code**<br> save this file for example in the components folder 
import React from 'react';
import './Weather.css';

const weekdays = [
  'Sunday',
  'Monday',
  'Tuesday',
  'Wednesday',
  'Thursday',
  'Friday',
  'Saturday',
];

const WeatherBox = ({ date, icon, temp }) => {
  const getDay = (date) => weekdays[new Date(date).getDay()];

  return (
    <div className="weather-Days">
      <h1>{date ? getDay(date) : ''}</h1>
      <img
        src={require(`../images/${icon || 'sunn1'}.svg`)}
        alt="weather icon"
      />
      <span className="temp">{Math.round(temp - 273.15)}°C</span>
    </div>
  );
};

export default Weather;<br>
