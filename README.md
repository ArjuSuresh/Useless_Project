# Useless_Project
Team Name: Black/White
Team Members: 
    Member 1: Arjun Suresh - Adi Shankara Institute of Engineering & Technology, Kalady
    Member 2: Adwaidh AS - Adi Shankara Institute of Engineering & Technology, Kalady

Project Description

Our project is an e-commerce website that has many things to choose and order from.
The Problem the website does not allow you to buy any items when you place your order.

[What ridiculous problem are you solving?]: How to create an engaging, user-friendly online shopping interface.
The Solution (that nobody asked for): Our code provides a visual, interactive, and category-driven UI for browsing and selecting products, addressing several key e-commerce UI/UX problems.

[How are you solving it? Keep it fun!]
Technical DetailsGreat —

 Problem #1: Product Discovery via Categories

Technical Solution:
 HTML:

The sidebar (.categories) includes a list of clickable <li> elements like:
<ul>
  <li onclick="filterProducts('electronics')">Electronics</li>
  ...
</ul>


JavaScript (assumed to be added):

* When users click a category, JavaScript will:

  1. Capture the category name.
  2. Filter displayed product cards (matching `data-category` attribute).
  3. Show only matching products, hide others.

 Each product card will include `data-category="electronics"` (or similar), which JS uses to match items to the selected category.

 Problem #2: Interactive & Attractive Product Display

Technical Solution:

HTML:

Each product is represented by a div.card:

 <div class="card" data-category="electronics">
  <div class="card-inner">
    <div class="card-front">
      <img src="images/speaker1.jpg">
      ...
    </div>
    <div class="card-back">
      <button>Add to Cart</button>
    </div>
  </div>
</div>


CSS:

* 3D flip animation is implemented via:

 .card-inner {
  transition: transform 0.6s;
  transform-style: preserve-3d;
}
.card:hover .card-inner {
  transform: rotateY(180deg);
}


Front and back of the card are absolutely positioned and hidden/revealed using transform: rotateY.

Effect:

* Makes product listings **interactive**, **memorable**, and **modern** — all of which boost engagement.



 Problem #3: Add-to-Cart Interaction

Technical Solution:

HTML:

* On the back of each card:

 <button>Add to Cart</button>


* There's a placeholder for the cart in the DOM:

 <div class="cart">
  <h2>Cart</h2>
  <ul id="cart-items"></ul>
  <button class="clear-cart">Clear Cart</button>
</div>


JavaScript (to be added):

* On clicking "Add to Cart", JS will:

  1. Clone the item info (title, price).
  2. Append it to the `<ul id="cart-items">`.
  3. Optionally store it in `localStorage`.

* Clicking “Clear Cart” will:

  * Empty the list.
  * Clear any stored cart data.

---

 Problem #4: Search Functionality

Technical Solution:

HTML:

* A search bar:

 <input type="text" id="search-bar" placeholder="Search products...">


JavaScript (to be added):

Add keyup event listener:

  * For each card, compare the search query to product title (case-insensitive).
  * Show/hide cards accordingly.

document.getElementById('search-bar').addEventListener('keyup', function() {
  const query = this.value.toLowerCase();
  document.querySelectorAll('.card').forEach(card => {
    const title = card.querySelector('h3').textContent.toLowerCase();
    card.style.display = title.includes(query) ? 'block' : 'none';
  });
});


---

Problem #5: Modern, Mobile-Friendly UI

Technical Solution:

 CSS:

 Uses **Flexbox** and **responsive units** (`vw`, `%`) to handle layout:

 .main {
  display: flex;
}
.categories {
  width: 20vw;
}
.products {
  width: 80vw;
  display: flex;
  flex-wrap: wrap;
}

  ```

 Animations, shadows, and transitions make UI smooth:

.card {
  transition: transform 0.3s ease, box-shadow 0.3s ease;
}
.card:hover {
  transform: scale(1.05);
}


  ```

* Consistent color scheme (black background, gold/orange highlights):

  * Helps build brand identity.
  * Enhances accessibility through contrast.

---

Summary: What We’ve Solved, Technically

| Problem                     | Solution                           | Technologies Used         |
| --------------------------- | ---------------------------------- | ------------------------- |
| Product categorization      | Category sidebar + filter          | HTML + JS (planned)       |
| Boring product presentation | Flip-cards, animations             | HTML + CSS                |
| No cart interaction         | Add-to-cart buttons + cart section | HTML + JS (planned)       |
| Hard to find items          | Search bar                         | HTML + JS (planned)       |
| Dull, non-responsive UI     | Modern layout + visual effects     | CSS Flexbox + transitions |

---


Technologies/Components Used

For Software:

  Languages used: HTML5, CSS3, JavaScript
  Frameworks used:Project is built with plain HTML/CSS/JS, 
  Libraries used:	All logic is done using Vanilla JavaScript
  Tools used:Text Editor (VS Code), Web Browser (Chrome),Developer Tools (F12), Local File System or Git,Photoshop / Canva

For Hardware:

  List main components:Computer/Laptop, Monitor (for multitasking (design/code/test), Keyboard & Mouse, Internet Connection, Smartphone/Tablet 
  List specifications:
  List tools required: VS Code, Git / GitHub, Design Tool (Figma, Photoshop, Canva)

Implementation

For Software:This project implements a responsive product page of an e-commerce website using front-end technologies. It includes product details, image gallery, pricing, quantity control, cart functionality, and responsive design.
Installation: Steps to Install:

 Download ZIP

   Download and unzip the project folder.

   Open the folder in your browser or code editor.

git clone https://github.com/your-username/ecommerce-product-page.git
cd ecommerce-product-page


commands:
Run



Run Command

If using VS Code + Live Server:

# No command needed — just:
Right-click on index.html → "Open with Live Server"


---

If using only the terminal (with Python installed):

For Python 3:
python -m http.server


Then open your browser and go to:
[http://localhost:8000](http://localhost:8000)

---


[commands]
Project Documentation
Here’s a simple and clear section you can add to your **Project Documentation** under **Commands**:

---

Commands

 1. Install Dependencies

If your project has dependencies (e.g., using `npm` or `pip`), run:

npm install
# or
pip install -r requirements.txt

---
 2. Run the Project
For Static Frontend (HTML/CSS/JS)

    Open index.html directly in your browser
    OR

    Run a simple local server:
   python -m http.server

Then open `http://localhost:8000` in your browser.

For Node.js Backend (if applicable)

node app.js
# or
npm start


---

3. Build Project (If applicable)

npm run build


---


For Software:
Screenshots (Add at least 3)

<img width="1902" height="956" alt="image" src="https://github.com/user-attachments/assets/1262eca8-4209-4a30-ba67-a72a955e4add" />(This is an e-commerce website which lets you place order but does not actually allow you to but items)

<img width="1915" height="936" alt="image" src="https://github.com/user-attachments/assets/bb81af4f-6009-43a6-8fcb-952960c0de49" />


<img width="1915" height="932" alt="image" src="https://github.com/user-attachments/assets/c3feb71e-62ef-4376-8dea-8f8cb20e7a15" />



Made with ❤️ at TinkerHub Useless Projects
