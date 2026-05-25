# Ex04 Simple Calculator - React Project
## Date:

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
app.jsx
```
import { useState } from "react";
import "./App.css";

function App() {
  const [result, setResult] = useState("");

  const handleClick = (value) => {
    setResult(result + value);
  };

  const clearResult = () => {
    setResult("");
  };

  const calculate = () => {
    try {
      setResult(eval(result).toString());
    } catch {
      setResult("Error");
    }
  };

  return (
    <div className="container">
      <div className="calculator">
        <h1>React Calculator</h1>

        <input type="text" value={result} readOnly />

        <div className="buttons">
          <button onClick={clearResult}>C</button>
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
          <button onClick={calculate}>=</button>

          <button onClick={() => handleClick("1")}>1</button>
          <button onClick={() => handleClick("2")}>2</button>
          <button onClick={() => handleClick("3")}>3</button>
          <button onClick={() => handleClick("0")}>0</button>
        </div>

        <footer>
          <p>
            Created by K. Dhanusri Pooja | Register No: 212224040068
          </p>
        </footer>
      </div>
    </div>
  );
}

export default App;
```

app.css
```
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  font-family: Arial, sans-serif;
}

body {
  background: linear-gradient(to right, #1e3c72, #2a5298);
}

.container {
  height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
}

.calculator {
  background: white;
  padding: 30px;
  border-radius: 15px;
  width: 320px;
  text-align: center;
  box-shadow: 0px 5px 20px rgba(0, 0, 0, 0.3);
}

.calculator h1 {
  margin-bottom: 20px;
  color: #1e3c72;
}

.calculator input {
  width: 100%;
  height: 60px;
  margin-bottom: 20px;
  text-align: right;
  font-size: 24px;
  padding: 10px;
  border: 2px solid #ccc;
  border-radius: 10px;
}

.buttons {
  display: grid;
  grid-template-columns: repeat(4, 1fr);
  gap: 10px;
}

.buttons button {
  padding: 18px;
  font-size: 18px;
  border: none;
  background: #1e3c72;
  color: white;
  border-radius: 10px;
  cursor: pointer;
  transition: 0.3s;
}

.buttons button:hover {
  background: #2a5298;
}

footer {
  margin-top: 20px;
  font-size: 14px;
  color: #555;
}
```



## OUTPUT
<img width="1919" height="1110" alt="image" src="https://github.com/user-attachments/assets/b63373b8-7eee-4259-875f-de049fd0e6ba" />
<img width="1919" height="1120" alt="image" src="https://github.com/user-attachments/assets/d456be65-d825-4ee5-960d-795c24be2588" />


## RESULT
The program for developing a simple calculator in React.js is executed successfully.
