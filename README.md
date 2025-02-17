### **Assignment: Building an Interactive and Dynamic Web Page**  

#### **Objective**  
Create a visually engaging and interactive webpage that utilizes **CSS3 transitions and animations**, **advanced JavaScript functions** (including scope, parameters, and return values), and combines **CSS animations with JavaScript** to create dynamic user interactions.  

---

### **Part 1: CSS3 Transitions and Animations**  
1. **Task**:  
   - Use **CSS transitions** to create smooth effects on hover or focus (e.g., buttons that change color or grow).  
   - Use **CSS animations** with `@keyframes` to create dynamic effects like fading, sliding, or rotating.
  
   - <!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>CSS Transitions Example</title>
  <style>
    .button {
      padding: 10px 20px;
      font-size: 16px;
      background-color: #3498db;
      color: white;
      border: none;
      border-radius: 5px;
      cursor: pointer;
      transition: all 0.3s ease; 
    }

    .button:hover {
      background-color: #2ecc71; 
      transform: scale(1.1);
    }
  </style>
</head>
<body>
  <button class="button">Hover Me</button>
</body>
</html>

- Use **CSS animations** with `@keyframes` to create dynamic effects like fading, sliding, or rotating.

<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>CSS Animation Example</title>
  <style>
    .box {
      width: 100px;
      height: 100px;
      background-color: #e74c3c;
      animation: fadeAndRotate 3s infinite ease-in-out; 
    }


    @keyframes fadeAndRotate {
      0% {
        opacity: 0; 
        transform: rotate(0deg);
      }
      50% {
        opacity: 1;
        transform: rotate(180deg); 
      }
      100% {
        opacity: 0; 
        transform: rotate(360deg); 
      }
    }
  </style>
</head>
<body>
  <div class="box"></div>
</body>
</html>


2. **Requirements**:  
   - At least **two elements** must include hover or focus transitions.  
   - At least **two animations** must be created using `@keyframes` (e.g., an animated banner or an animated loading spinner).  

---

<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>CSS Transitions and Animations</title>
  <style>
    .button1 {
      padding: 10px 20px;
      font-size: 16px;
      background-color: #3498db;
      color: white;
      border: none;
      border-radius: 5px;
      cursor: pointer;
      transition: all 0.3s ease;
    }

    .button1:hover {
      background-color: #2ecc71;
      transform: scale(1.1);
    }

    .button2 {
      padding: 10px 20px;
      font-size: 16px;
      background-color: #9b59b6;
      color: white;
      border: none;
      border-radius: 5px;
      cursor: pointer;
      transition: background-color 0.3s ease;
    }
    .button2:hover {
      background-color: #8e44ad;
    }

    @keyframes slideIn {
      0% {
        transform: translateX(-100%);
        opacity: 0;
      }
      100% {
        transform: translateX(0);
        opacity: 1;
      }
    }

    .banner {
      width: 100%;
      height: 50px;
      background-color: #f39c12;
      color: white;
      text-align: center;
      line-height: 50px;
      font-size: 20px;
      animation: slideIn 2s ease-out forwards;
    }

    @keyframes rotateSpinner {
      0% {
        transform: rotate(0deg);
      }
      100% {
        transform: rotate(360deg);
      }
    }

    .spinner {
      margin: 50px auto;
      width: 50px;
      height: 50px;
      border: 5px solid #3498db;
      border-top: 5px solid transparent;
      border-radius: 50%;
      animation: rotateSpinner 1s linear infinite;
    }

  </style>
</head>
<body>
 
  <button class="button1">Button 1 - Hover Me</button>
  <button class="button2">Button 2 - Hover Me</button>

  
  <div class="banner">Welcome to Our Website!</div>


  <div class="spinner"></div>
</body>
</html>


### **Part 2: JavaScript Functions**  
1. **Task**:  
   - Write JavaScript functions to handle interactivity on the webpage.  
   - Utilize **parameters**, **return values**, and demonstrate an understanding of **scope**.  

2. **Requirements**:  
   - Write at least **three functions**:  
     - A function with parameters and return values (e.g., calculate a value like the area of a rectangle based on user input).  
     - A function that demonstrates the concept of scope (local vs. global variables).  
     - A function to toggle a CSS class that applies an animation (e.g., toggling a "hidden" class for a modal).  


<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>JavaScript Functions Example</title>
  <style>
    .modal {
      display: none;
      width: 300px;
      height: 200px;
      background-color: #f39c12;
      color: white;
      text-align: center;
      line-height: 200px;
      position: absolute;
      top: 50%;
      left: 50%;
      transform: translate(-50%, -50%);
      font-size: 20px;
      border-radius: 10px;
      transition: opacity 0.5s ease-in-out;
    }

    .modal.hidden {
      display: none;
      opacity: 0;
    }

    button {
      padding: 10px 20px;
      font-size: 16px;
      margin: 10px;
      cursor: pointer;
      background-color: #3498db;
      color: white;
      border: none;
      border-radius: 5px;
    }
  </style>
</head>
<body>

  <button onclick="calculateArea(5, 10)">Calculate Area of Rectangle</button>
  <button onclick="toggleModal()">Toggle Modal</button>
  
  <div class="modal" id="myModal">This is a modal</div>

  <script>
    function calculateArea(length, width) {
      const area = length * width;
      alert('Area of rectangle: ' + area + ' square units');
      return area; 
    }

    let globalVar = "I am a global variable";

    function demonstrateScope() {
      let localVar = "I am a local variable"; 
      alert(globalVar);
      alert(localVar); 
    }

   
    function toggleModal() {
      const modal = document.getElementById('myModal');
      modal.classList.toggle('hidden'); 
    }
  </script>

</body>
</html>

---

### **Part 3: Combining CSS Animations with JavaScript**  
1. **Task**:  
   - Use JavaScript to trigger or control CSS animations dynamically.  

2. **Requirements**:  
   - Create an interactive element (e.g., a button, card, or slider) that triggers an animation when clicked.  
   - Dynamically add or remove CSS classes to control the animation.  
   - Ensure that the animation resets properly when triggered multiple times.
  
   <!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>CSS Animations with JavaScript</title>
  <style>
    .card {
      width: 200px;
      height: 300px;
      background-color: #3498db;
      color: white;
      text-align: center;
      line-height: 300px;
      font-size: 20px;
      border-radius: 10px;
      position: relative;
      transition: transform 0.5s ease, opacity 0.5s ease;
    }

    @keyframes bounce {
      0% {
        transform: scale(1);
      }
      25% {
        transform: scale(1.2);
      }
      50% {
        transform: scale(1);
      }
      75% {
        transform: scale(1.1);
      }
      100% {
        transform: scale(1);
      }
    }

    .bounce-animation {
      animation: bounce 1s ease-out forwards;
    }

    button {
      padding: 10px 20px;
      font-size: 16px;
      background-color: #2ecc71;
      color: white;
      border: none;
      border-radius: 5px;
      cursor: pointer;
      margin-top: 20px;
    }

  </style>
</head>
<body>

  <div class="card" id="card">Click the Button</div>

  <button onclick="triggerAnimation()">Animate Card</button>

  <script>
    function triggerAnimation() {
      const card = document.getElementById('card');
      
      card.classList.remove('bounce-animation');
      
      void card.offsetWidth; 

      card.classList.add('bounce-animation');
    }
  </script>

</body>
</html>


---
