# Custom Widget Template
## Description
Template project to set up a custom widget with vue + vueform + blocksdk. 
## Clone and install
* create a new repository and write down the remote url
* `git clone ...` to clone this repository
* `git remote set-url origin <your.new.origin>` to set the remote to your new repository
* `yarn` to install
* `yarn dev` to run the dev server
## How to work with this project
A Custom Widget consists of two components:
* The UI, that is displayed on left side of the content builder
* The content, that is redered, when you input data into the UI
In this project the UI is built with a vueform object in `/src/App.vue`. You can add new inputs and change the appearance of the UI by updating that object. Check the vueform [docs](https://vueform.com/docs/rendering-forms#using-schema-object) for more information.
The content will be built inside the template section of `/src/App.vue`, inside the #widget-content div. 
Add a new input to the vueform element: 
```javascript
...
newInput: {
      type: 'text',
    },
...
```
and reference the value in your template section:
```
...
<p>{{ formValues.newInput }}</p>
...
```
