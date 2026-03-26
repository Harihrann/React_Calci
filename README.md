# Ex04 Simple Calculator - React Project
## Date: 26 / 03 / 2026

```
Name : Hariharan S
Reg no : 21222404101

```

## AIM
To  develop a Simple Calculator using React.js with clean and responsive design, ensuring a smooth user experience across different screen sizes.

## ALGORITHM
### STEP 1
Create a React App.

### STEP 2
Open a terminal and run:
  <ul><li>npx create-react-app simple-calculator</li>
  <li>cd simple-calculator</li>
  <li>npm start</li></ul>

### STEP 3
Inside the src/ folder, create a new file Calculator.js and define the basic structure.

### STEP 4
Plan the UI: Display screen, number buttons (0-9), operators (+, -, *, /), clear (C), and equal (=).

### STEP 5
Create a new file Calculator.css in src/ and add the styling.

### STEP 6
Open src/App.js and modify it.

### STEP 7
Start the development server.
  npm start

### STEP 8
Open http://localhost:3000/ in the browser.

### STEP 9
Test the calculator by entering numbers and operations.

### STEP 10
Fix styling issues and refine content placement.

### STEP 11
Deploy the website.

### STEP 12
Upload to GitHub Pages for free hosting.

## PROGRAM

### Calculator.js

```
import { useState } from "react";
import "./Calculator.css";

export default function Calculator() {
  const [input, setInput] = useState("");

  const handleClick = (value) => {
    setInput(input + value);
  };

  const handleClear = () => {
    setInput("");
  };

  const handleEqual = () => {
    try {
      setInput(eval(input).toString());
    } catch {
      setInput("Error");
    }
  };

  return (
    <div className="calculator">
      <input type="text" value={input} readOnly className="display" />

      <div className="buttons">
        <button onClick={handleClear}>C</button>
        <button onClick={() => handleClick("/")}>/</button>
        <button onClick={() => handleClick("*")}>*</button>
        <button onClick={() => handleClick("-")}>-</button>

        <button onClick={() => handleClick("7")}>7</button>
        <button onClick={() => handleClick("8")}>8</button>
        <button onClick={() => handleClick("9")}>9</button>
        <button onClick={() => handleClick("+")}>+</button>

        <button onClick={() => handleClick("4")}>4</button>
        <button onClick={() => handleClick("5")}>5</button>
        <button onClick={() => handleClick("6")}>6</button>
        <button onClick={handleEqual}>=</button>

        <button onClick={() => handleClick("1")}>1</button>
        <button onClick={() => handleClick("2")}>2</button>
        <button onClick={() => handleClick("3")}>3</button>

        <button onClick={() => handleClick("0")} className="zero">
          0
        </button>
      </div>
    </div>
  );
}
```

### Calculator.css

```
body {
  background: #000;
  display: flex;
  justify-content: center;
  align-items: center;
  height: 100vh;
  font-family: Arial, sans-serif;
}

.calculator {
  background: #111;
  padding: 20px;
  border-radius: 10px;
  box-shadow: 0 0 10px #fff;
  width: 260px;
}

.display {
  width: 100%;
  height: 50px;
  background: #000;
  color: #fff;
  border: none;
  text-align: right;
  font-size: 24px;
  margin-bottom: 10px;
  padding: 10px;
}

.buttons {
  display: grid;
  grid-template-columns: repeat(4, 1fr);
  gap: 10px;
}

button {
  height: 50px;
  background: #fff;
  color: #000;
  border: none;
  font-size: 18px;
  cursor: pointer;
  border-radius: 5px;
}

button:hover {
  background: #ccc;
}

.zero {
  grid-column: span 4;
}
```


## OUTPUT
<img width="1919" height="1198" alt="image" src="https://github.com/user-attachments/assets/c1ca6977-6c1e-43bd-bb95-25e917f56e44" />


## RESULT
The program for developing a simple calculator in React.js is executed successfully.
