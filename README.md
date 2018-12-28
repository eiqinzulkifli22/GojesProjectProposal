GROUP MEMBER
NURUL ASYIQIN BINTI ZULKIFLI 1525192
NURUL IZZATI BINTI MUSLIM 1521836
NUR ARIFFAH BINTI RAMLI 1528604
SITI NUR AMIRAH AMINAH BINTI ZULKEFLEY 1525638

# CalorieTracker

### 1.1 INTRODUCTION
The application that we are going to develop is mobile application and the name is given as Calorie Tracker. The target users of this system is public people and for those who concern about their health especially daily calorie intake. We plan to do several functions such as scan the food calories, calculate the user’s calorie intake and calculate the calorie burns by pedometer. More details will be explain in this proposal below.

### 1.2 PROBLEM DESCRIPTION
#### 1.2.1  Background of the problem
 
The system intended to be developed is a mobile application while the target users will be men and women who are concern with their calories intake and burned. Normally, when people take their meal, they are unaware of the calorie amount. This can be detrimental because ones might take too much calories while ones might consume too little calories for their body. Moreover, the calories intake for each individual is different according to some factors for instance age, gender, weight and exercise level.

#### 1.2.2 Problem Statement 
Sometimes it is hard to locate the calories of food products due to too many information on the products’ cover/ packaging/ plastic and the font used can be too small to read. The information provided on the foods’ packaging does not include how many calories intake is suitable for each individual. It takes time to calculate manually the number of calories needed and burned for each person.

### 1.3 PROJECT OBJECTIVE
The objective of this project is to develop a mobile application that help users to have a healthy lifestyle by providing some functions such as counting the amount of calories intake and burned. Apart from that, the application is intended to ease the users to know the number of calories of a particular food in a more convenient way, which is by scanning the barcode. Generally, the apps to be developed will be a simple apps with minimalist design, easy to use and small in storage. The report that will be produced is the Final Project Report.

### 1.4 PROJECT SCOPE
#### 1.4.1 Scope
Calorie Tracker is a system that will help its user to use a mobile application in order to track the calorie intake and calorie burned in a day.

#### 1.4.2 Targeted User
The application is developed to assist men and women who are concerned about eating healthy, loves exercising and also those who want to lose weight as this application will help to monitor the calorie intake as well as calorie burned in a day. 

#### 1.4.3 Specific Platform
In developing Calorie Tracker, Android platform will be used in order to develop this project and Visual Studio Code from Microsoft for the tools as it is a free tools for developers, ES6 react-native, expo app and node.js

### 1.5 CONSTRAINTS
The constraints in developing this application will be limited machine because some of the team members use native code with emulator while the others are using expo app. Besides, other constraints will be skills in creating every function and combining them into one app.

### 1.6 PROJECT STAGES
Task 1: Prepare the proposal
Task date: 24/11/18 – 30/11/18
Milestone 1: 30/11/2018

Task 2: Analysis and Design
Task date: 1/12/18 – 7/12/18
Milestone 2: 7/11/18

Task 3: Development
Task Date: 8/12/18-28/12/18
Milestone 3: 14/12/18
Mielstone 4: 21/12/18

Task 4: Presentation
Task date: expected date (31/12/18)

Task 5: Submission
Task date: expected date (31/12/18)
Milestone 5: 28/12/18

### 1.7 SIGNIFICANCE OF THE PROJECT

The significance of Calorie Tracker will benefit:
- Males or females who want to keep track of their calories with this portable mobile application.
- People who want to know the total number of calories for a specific food or the food they will consume.
- Making life easier for the people who wants to know how many calories burned in each day.
- Give concern and awareness to the people about their healthy lifestyle.

### 1.8 SUMMARY
In conclusion, the Calorie Tracker is an app to help the user maintain a healthy lifestyle by monitoring their calorie intake and calorie burned. The current process of calorie tracking is confusing and hard to understand for them. Based on the problem, we are aiming to develop a proper platform for the user to calculate and observe their daily calorie intake. Not only that, the targeted users and platform to develop this app is also stated with the project stages to plan and keep track on our progress. We hope this project will become successful and useful for the targeted user.

### 1.9 PROJECT DEVELOPMENT

Project Name: CalorieTracker

//App.js

import React, { Component } from "react";
import { createStackNavigator, createAppContainer } from "react-navigation";
import HomeScreen from "./HomeScreen";
import CalcScreen from "./CalcScreen";
import FoodListScreen from "./FoodListScreen";
import DietTipsScreen from "./DietTipsScreen";
import PedometerScreen from "./PedometerScreen";
import FoodScannerScreen from "./FoodScannerScreen";

const RootStack = createStackNavigator(
  {
    Home: HomeScreen,
    Calculate: CalcScreen,
    FoodList: FoodListScreen,
    DietTips: DietTipsScreen,
    Pedometer: PedometerScreen,
    FoodScanner: FoodScannerScreen
  },
  {
    initialRouteName: 'Home'
  }
);

const AppContainer = createAppContainer(RootStack);


export default class App extends Component {
  render() {
    return (
       <AppContainer />
    
    );
  }
}

import React, { Component } from "react";
import { createStackNavigator, createAppContainer } from "react-navigation";
import HomeScreen from "./HomeScreen";
import CalcScreen from "./CalcScreen";
import FoodListScreen from "./FoodListScreen";
import DietTipsScreen from "./DietTipsScreen";
import PedometerScreen from "./PedometerScreen";
import FoodScannerScreen from "./FoodScannerScreen";


const RootStack = createStackNavigator(
  {
    Home: HomeScreen,
    Calculate: CalcScreen,
    FoodList: FoodListScreen,
    DietTips: DietTipsScreen,
    Pedometer: PedometerScreen,
    FoodScanner: FoodScannerScreen
  },
  {
    initialRouteName: 'Home'
  }
);

const AppContainer = createAppContainer(RootStack);


export default class App extends Component {
  render() {
    return (
       <AppContainer />
    
    );
  }
}


// FoodListScreen.js

import React, { Component } from "react";
import { Container,  Content, Accordion , Header} from "native-base";
import { AppRegistry, ScrollView, Image, Text } from 'react-native';

const dataArray = [
 
  { title: "Beef Rendang ", content: "Food Calorie: 468 kcal/ serving"  },
  { title: "Cendol", content: "Food Calorie: 335 kcal/ serving" },
  { title: "Creamer Milk", content: "Food Calorie: 63 kcal/ 1 table spoon" },
  { title: "Char Kue Tiau", content: "Food Calorie: 740 kcal/ serving" },
  { title: "Fried Chicken", content: "Food Calorie: 290 kcal/ piece" },
  { title: "Half Boiled Egg with Plain Bread", content: "Food Calorie: 227 kcal/ piece" },
  { title: "Mee Goreng Mamak", content: "Food Calorie: 660 kcal/ serving" },
  { title: "Mee Soup", content: "Food Calorie: 381 kcal/ serving" },
  { title: "Nasi Ayam ", content: "Food Calorie: 660 kcal/ serving" },
  { title: "Nasi Kerabu ", content: "Food Calorie: 360 kcal/ serving" },
  { title: "Nasi Lemak", content: "Food Calorie: 587 kcal/ serving" },
  { title: "Laksa ", content: "Food Calorie: 400 kcal/ serving" },
  { title: "Rice", content: "Food Calorie: 130 kcal/ 100 grams" },
  { title: "Roti Canai & Dal ", content: "Food Calorie: 360 kcal/" },
  { title: "Teh Tarik", content: "Food Calorie: 249 kcal/ 1 table spoon" }
  
];

export default class FoodListScreen extends Component {

  render() {
    return (
        <ScrollView>
      <Container>
 
        <Content padder>
        <Text style={{ fontSize: 20, marginTop: 10, marginBottom: 20}}>Food Calorie Lists</Text>
          <Accordion dataArray={dataArray}
           headerStyle={{ backgroundColor: "#D4BFE0" , marginTop: 10}}
           contentStyle={{ backgroundColor: "#f3f6f7" }}
           
          />
         
         
        </Content>
  
      </Container>
      </ScrollView>
    );
  }
}












