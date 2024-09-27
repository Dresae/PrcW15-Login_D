 
#  Responsive Login Form
Responsive Login form with React.js

![screenshot](pics/screenshot1.png)
>

#  Setting up the project
 
##  Initialize the project
Through Vite we will create a React App template on the terminal:

***
```console
npm create vite@latest ./ -- --template react
```
_Install dependencies and start development server_
```console
npm install
npm run dev
```

## Prepare your environment
- For this instance we are not going to use the **assets** folder and the **app.css** file, so they are removed.

- Download the logos in **.svg** format and place them directly on the public folder 

- Add the link of the Google font family later used for the icons and fonts in the **index.html** file
***

# Building up the components

## 1. SocialLogin.jsx component
In the **SocialLogin.jsx** we define the layout and functionalities of the Login form. This is done by declaring the **SocialLogin** variable and establishing one container under the class **social-login** for both the **Google button** and the **Apple button**

## 2. InputField.jsx component
Here we are integrating a reusable React component called **InputField**, which is customizable and can be used for different types of inputs.

Though this component we included icons and a toggle feature to show or hide the password characters.

## Code breakdown

***
-  **Importing _useState_ from React**
>
```js
import { useState } from "react";
```

> 
***

-  **Code section title 2**
>
```css
Put your code here exactly as it is.
```

> Use this text block to describe **relevant facts**, features or functions of your CSS code section that you consider will be useful in understanding **how the style was applied** and its relationship with the HTML code. You **highlight** some parts of this text to **improve its readability**.
***


![reading...](https://media.giphy.com/media/Tf3mp01bfrrUc/giphy.gif?cid=ecf05e47wajghtrc5targr7mju7coe0avdyurnehrr1krgdt&ep=v1_gifs_search&rid=giphy.gif&ct=g "...How could I ever do so unless someone guide me?")

***