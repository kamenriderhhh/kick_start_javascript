# Instructions for Kick Starting JavaSript

#### 1. Copy the following files to your desired project location.

> [index.html](./resource/index.html)<br>
> [main.css](./resource/main.css)<br>

---

#### 2. Link to javascript, copy the following code to your index.html file just before the ```</body>```  

``` html
<script src="app.js"></script>
<noscript>The JavaScript is deactivated in this site.</noscript>
 ```

The ```<script>``` element can be placed in the ```<head>``` element or elsewhere in ```<body>``` element.

In this tutorial we place it just before the closing of ```<body>``` element is to make sure all page content display first before loading the script.

The ```<noscript>``` element placed after the ```</script>``` which will show a message if JavaScript is deactivated. This is also known as ***Fault Tolerance***

---

### 3. Create app.js in the same directory and place the following code in the very top.

 ``` js 
 'use strict'
 ```

---

### 4. Then go back to the index.html to add a button for changing the theme.

 ``` html
 ...
<ul>
  <li class="list">Add visual styles</li>
  <li class="list">Add light and dark themes</li>
  <li>Enable switching the theme</li>
</ul>
<div>
  <button class="btn">Dark</button>
</div>
<script src="app.js"></script>
... 
```

---

### 5. Add an event handler to app.js it will look like belows:

``` js
'use strict'

const switcher = document.querySelector(".btn");

switcher.addEventListener('click', function() {
    document.body.classList.toggle('dark-theme')

    var className = document.body.className;
    if(className == "light-theme") {
        this.textContent = "Dark";
    }
    else {
        this.textContent = "Light";
    }

    console.log('current class name: ' + className);

});
```

Open developer tool by **pressing F12** in browser and go to **console tab** we will be able to see the body class name changes.



