### **Module 1: The Foundation - Structuring and Styling the Web**

#### **Lesson 1: Introduction & Setup**

**Goal:** By the end of this lesson, you will understand the roles of a client and a server, have a complete local development environment installed, and run both a basic HTML and a basic PHP file on your computer.

---

#### **Part 1: The Concepts - The Client/Server Dance**

Welcome to your first step in becoming a full-stack developer! But what does "full-stack" even mean?

Imagine you're at a restaurant.

*   You, the **customer**, are the **Client**. You sit at your table (your web browser) and make a request for food (you type in `www.google.com`).
*   The **Waiter** is the **Internet**. They take your request from your table to the kitchen.
*   The **Kitchen** is the **Server**. This is a powerful computer that receives the request, prepares your order (fetches data, runs logic), and gives it back to the waiter.
*   The **Waiter** (Internet) brings the food (the website data) back to your table (your browser), where it's displayed for you to enjoy.

A **Front-End Developer** specializes in what the customer sees and interacts with—the restaurant's decor, the menu layout, the presentation of the food. This is **HTML, CSS, and JavaScript**.

A **Back-End Developer** specializes in the kitchen—the ovens, the ingredients, the recipes, the database of orders. This is **PHP and MySQL**.

A **Full-Stack Developer** understands the entire process, from the customer's request to the kitchen's preparation and back. They can build both the front-end and the back-end. That's what you are here to become.

---

#### **Part 2: The Setup - Your Development Kitchen**

Now, let's build our local development "kitchen." We need to install all the tools a professional developer uses.

##### **1. The Code Editor: Visual Studio Code**

This is where you will write all your code. It's like your chef's knife set—versatile and essential.
*   **Action:** Download and install VS Code from the official website.

##### **2. The Back-End Engine: XAMPP or MAMP**

![XAMPP vs MAMP](/assets/xampp-vs-mamp.jpg)

This package gives us our **server kitchen** in one easy installation. It includes:
*   **A**pache: Our web server. The "head chef" that handles requests.
*   **M**ySQL: Our database. The "pantry" where we store data.
*   **P**HP: Our back-end language. The "recipe book" the chef follows.
*   **P**erl: (We won't be using this).

*   **Action:**
    *   If you are on **Windows or Linux**, download and install **XAMPP**.
    *   If you are on a **Mac**, download and install **MAMP**.
*   **Search for:** "Download XAMPP" or "Download MAMP".
*   **After Installing:** Open the XAMPP or MAMP control panel. You will see a list of services. Press **Start** for both **Apache** and **MySQL**. If they turn green, you are ready to go!

##### **3. The Front-End Helper: Node.js and npm**

![Node.JS](/assets/nodejs.jpg)

We are *not* going to write Node.js code, but we need it for one very important tool: **`npm`** (Node Package Manager). We will use `npm` to install a **live server**, which automatically reloads our web page when we save our HTML or CSS. This will make front-end development much faster.

*   **Action:** Download and install Node.js from the official website. The "LTS" (Long-Term Support) version is recommended.
*   **Search for:** "Download Node.js".
*   **Verify Installation:** Open a new terminal (or Command Prompt on Windows) and type the following commands, pressing Enter after each one:
    ```bash
    node -v
    npm -v
    ```
    If you see version numbers for both, the installation was successful!

---

#### **Part 3: First Steps - Running Your Code**

##### **Your Project Folder: `htdocs`**

Apache, our web server, doesn't look at every file on your computer. It only serves files from a special folder.
*   For **XAMPP**, this folder is located at `C:\xampp\htdocs`.
*   For **MAMP**, this folder is located at `/Applications/MAMP/htdocs`.

This `htdocs` folder is your server's "public" directory. Everything we build will go inside a new folder we create here.

1.  Navigate to your `htdocs` folder.
2.  Create a new folder inside it called `fullstack-crashcourse`.
3.  Open this `fullstack-crashcourse` folder with VS Code. This will be our project's home.

##### **Running PHP: The Server Way**

Let's create our first PHP file to prove our Apache server is working.

1.  In VS Code, inside your `fullstack-crashcourse` folder, create a new file named `hello.php`.
2.  Type the following code into the file and save it:
    ```php
    <!DOCTYPE html>
    <html lang="en">
    <head>
        <title>My First PHP Page</title>
    </head>
    <body>
        <h1><?php echo "Hello from the Server!"; ?></h1>
        <p>This page was processed by Apache and PHP.</p>
    </body>
    </html>
    ```
3.  **To view this page, you MUST go through the server.** Open your web browser and navigate to:
    `http://localhost/fullstack-crashcourse/hello.php`

You should see a page with the heading "Hello from the Server!". The `<?php ... ?>` block was executed by the server *before* the page was sent to your browser. If you "View Page Source" in your browser, you will not see the PHP code, only the final HTML output. This is a critical concept!
![Hello from the server message](/assets/lesson-1.1-hello.jpg)

---

### **Mini-Challenge!**

Now it's your turn.

1.  Create a new file in your project folder named `challenge.php`.
2.  Inside this file, use the PHP `echo` command and the `date()` function to display a message with the current date.
3.  The final output in your browser should be a sentence like: **Hello! Today is [current date]**. For example: *Hello! Today is 2025-07-28*.

**Hint:** The PHP `date()` function needs a format string. To get the Year-Month-Day format, you would use `date('Y-m-d')`.

Good luck!

---

### **What's Next?**

In the next lesson, we will get started on the front-end by learning how to structure a web page with semantic HTML, building the skeleton for our final blog project.