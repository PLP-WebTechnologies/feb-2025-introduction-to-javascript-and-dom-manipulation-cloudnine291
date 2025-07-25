index.html

<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Interactive Page</title>
  <link rel="stylesheet" href="style.css" />
</head>
<body>
  <header>
    <h1 id="main-title">Welcome to My Page</h1>
  </header>

  <nav>
    <ul>
      <li><a href="#">Home</a></li>
      <li><a href="#">About</a></li>
    </ul>
  </nav>

  <main>
    <section>
      <p id="text">Click the button to change this text and style.</p>
      <button id="change-btn">Change Text & Style</button>
    </section>

    <section>
      <button id="add-btn">Add Item</button>
      <button id="remove-btn">Remove Item</button>
      <ul id="item-list">
        <li>Item 1</li>
        <li>Item 2</li>
      </ul>
    </section>
  </main>

  <footer>
    <p>&copy; 2025 My Page</p>
  </footer>

  <script src="script.js"></script>
</body>
</html>

script.js

// Change text and style
const changeBtn = document.getElementById("change-btn");
const text = document.getElementById("text");

changeBtn.addEventListener("click", () => {
  text.textContent = "The text has been updated!";
  text.style.color = "green";
  text.style.fontWeight = "bold";
  text.style.background = "#f0f0f0";
});

// Add and remove list items
const addBtn = document.getElementById("add-btn");
const removeBtn = document.getElementById("remove-btn");
const list = document.getElementById("item-list");

addBtn.addEventListener("click", () => {
  const newItem = document.createElement("li");
  newItem.textContent = "New Item";
  list.appendChild(newItem);
});

removeBtn.addEventListener("click", () => {
  if (list.lastElementChild) {
    list.removeChild(list.lastElementChild);
  }
});


style.css
body {
  font-family: Arial, sans-serif;
  margin: 20px;
  line-height: 1.6;
}

button {
  margin-top: 10px;
  margin-right: 10px;
  padding: 8px 12px;
  cursor: pointer;
}



