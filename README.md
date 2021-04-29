# FoodCheck

## Table of Contents
1. [Overview](#Overview)
1. [Product Spec](#Product-Spec)
1. [Wireframes](#Wireframes)
2. [Schema](#Schema)

## Overview
### Description
Our app allows users to keep track of the expiration date of the perishable items in their house. The app will display how much longer they have to use the item and allow them to enter foods and expiration dates to be tracked. 


### App Evaluation
- **Category:** Health & Fitness / Lifestyle 
- **Mobile:** This app would be primarily developed for mobile but would perhaps be just as viable on a computer. Functionality wouldn’t be limited to mobile devices.
- **Story:** Keeps track of expiration dates of all perishable items. User can enter the expiration date into the app, and the app will display how much longer the user has to use the item.  
- **Market:** Any individual could choose to use this app. The target market would probably be young teens and above, or people just starting to learn how to cook. 
- **Habit:** The app could be used every day as the user would make different meals with different items day-to-day so they would have to constantly check the status of their food. 
- **Scope:** First, we would start with having the user enter manually the expiration dates. This could evolve into the user scanning the barcode of the item instead of having to manually enter it for easier access. This could be used in collaboration with the MyFridge app, or nutrition apps such as MyFitnessPal and Lose It! 

## Product Spec

### 1. User Stories (Required and Optional)

**Required Must-have Stories**

- [x] User can see all the items they have entered so far 
- [x] User can enter an expiration date and the food
- [x] User can see how many days they have left to use the product 
- [x] User can log in and sign up


## Video Walkthrough
Here's a walkthrough of implemented user stories:

<img src='http://g.recordit.co/wvP7lmgqaD.gif' title='Completed App' width='' alt='Completed App' />


**Optional Nice-to-have Stories**

* User can delete an expiration date and the food 
* Assign a color-coded value to each food depending on how long it has left.
* Food is categorized (dairy, grains, etc.) 

### 2. Screen Archetypes

* Food List Screen - User sees a list of food and its expiration date  
   * User can scroll through a list of the food and its expiration date.
   * User can view the list of foods from closest to expiration to farthest from expiration. 
   * ...
* Logging Screen - User can enter an expiration date 
   * Allows user to type in the expiration date of their product 
   * Allows user to type in what the food is.
   * ...

### 3. Navigation

**Tab Navigation** (Tab to Screen)

* Loggin in
* Logging food and date
* List of food and date

**Flow Navigation** (Screen to Screen)

* (For the optional user stories)
   * List of food and date -> Details about food 

## Wireframes
<img src="http://g.recordit.co/6uvAV4GBsy.gif" width=600>

### [BONUS] Digital Wireframes & Mockups
https://www.figma.com/file/C49QVujzta9dVIF3x45PGt/FoodCheck?node-id=0%3A1

### [BONUS] Interactive Prototype

## Schema 
[This section will be completed in Unit 9]
### Models
<table>
  <tr>
    <td>#Property</td>
     <td>#Type</td>
    <td>#Description</td>
  </tr>
  <tr>
    <td>image</td>
    <td>File</td>
    <td>the image associated with the category of the food</td>
  <tr>
    <td>food</td>
    <td>String</td>
    <td>the name of the food</td>
   <tr>
    <td>days</td>
    <td>Number</td>
    <td>the number of remaining days before the expiration date</td>
   <tr>
    <td>userId</td>
    <td>String</td>
    <td>the person that is logged in</td>
  </tr>
 </table>
 
### Networking
* List of network requests by screen 
  * Login Screen
    * (Read/GET) Query the user id
    * (Create/SIGNUP) Create a new user id
  * Viewing Food Screen
    * (Read/GET) Query foods listed
    * (Read/GET) Query foods expiration date / days left
    * (Read/GET) Query the category associated with the image
  * Logging Food Screen
    * (Create/POST) Create the food name
    * (Create/POST) Create the food expiration date / days remaining
    * (Create/POST) Create the food image
