 
#  Responsive Login Form
Responsive Login form with React.js

![screenshot](pics/screenshot1.png)
>

#  Setting up the project

***

##  Initialize the project
Through Vite we will create a React App template on the terminal:

```console
npm create vite@latest ./ -- --template react
```
_Install dependencies and start development server_
```console
npm install
npm run dev
```

***

## Prepare your environment
- For this instance we are not going to use the **assets** folder and the **app.css** file, so they are removed.

- Download the logos in **.svg** format and place them directly on the public folder 

- Add the link of the Google font family later used for the icons and fonts in the **index.html** file.

***

# Building up the components

## 1. SocialLogin.jsx component
In the **SocialLogin.jsx** we define the layout and functionalities of the Login form. This is done by declaring the **SocialLogin** variable and establishing one container under the class **social-login** for both the **Google button** and the **Apple button**

***

## 2. InputField.jsx component
Here we are integrating a reusable React component called **InputField**, which is customizable and can be used for different types of inputs.

Through this component we included icons and a toggle feature to show or hide the password characters.

***

# Code breakdown

-  **Importing _useState_ from React**
>
```js
import { useState } from "react";
```

This hook is used to add state to functional components.

***

-  **Defining the input field component**
>
```js
 const InputField = ({ type, placeholder, icon }) => {
```

The **inputField** is a functional component that takes three props: **type**, **placeholder** and **icon**.

***

-  **State to toggle password visibility**
>
```js
 const [isPasswordShown, setIsPasswordShown] = useState(false);
```

The component uses the **useState** hook to create  a state variable **isPasswordShown** with an initial value of **false**. This state is used to toggle the visibility of password characters.

***


-  **JSX Return statement**
>
```js
  return (
    <div className="input-wrapper">
      <input
        type={isPasswordShown ? 'text' : type}
        placeholder={placeholder}
        className="input-field"
        required
      />
      <i className="material-symbols-rounded">{icon}</i>
      {type === 'password' && (
        <i onClick={() => setIsPasswordShown(prevState => !prevState)} className="material-symbols-rounded eye-icon">
          {isPasswordShown ? 'visibility' : 'visibility_off'}
        </i>
      )}
    </div>
```

The component returns a **div** element with a class of **input-wrapper**, which is composed of three child elements:

1- **input Field**: Its **type** attribute is determined by the **isPasswordShown** state. If **isPasswordShown** is **true**, the type is set to **text**, otherwise it's set to the value of the **type** prop.

The **placeholder** text for the input field, set to the value of the **placeholder** prop

The **required** is a boolean attribute indiccating that the input field is required.

2- **icon**: An **i** element with a class of **material-symbols-rounded eye-icon**, which is only rendered if the **type** prop is set to **password**. This element toggle the **isPasswordShown** state when clicked and displays either the **visibility** or the **visibility_off** icon depending on the state. 
***

-  **Exporting the component**



```js
 export default InputField;
```
-**export**: This keyword is used to export the component built and making it available for import in other files.

-**default**: This keyboard specifies that the component being exported is the default export of the file. This means that when another file imports from this file, it will import this component by default, without needing to specify the name.

-**inputField**: Its the name of the component to be exported allowing other files to import and use this component in their code.

***

![reading...](https://media.giphy.com/media/Tf3mp01bfrrUc/giphy.gif?cid=ecf05e47wajghtrc5targr7mju7coe0avdyurnehrr1krgdt&ep=v1_gifs_search&rid=giphy.gif&ct=g "...How could I ever do so unless someone guide me?")

***