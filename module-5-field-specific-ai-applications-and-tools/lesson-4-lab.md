<!-- # **Lab: AI-Driven Web Development** -->

<br>

:::info
:information_source: Estimated completion time: 2 hours
:::

<br>

## **Lab Overview**

In this lab, you will use ChatGPT to identify and fix bugs in a provided web page code, and then add a simple AI-driven feature to the web page. Detailed step-by-step instructions will be provided.

## **Lab Objectives**

By the end of this lab, you will be able to:

- Utilize ChatGPT to identify and fix bugs in a web page code.
- Add a simple AI-driven feature to a web page.
- Document findings and create a report.

## **Setting Up the Lab Environment**

### Instructions for Accessing and Using ChatGPT

1. **Access ChatGPT:**

   - Go to [ChatGPT](https://chat.openai.com/).
   - If you don’t have an account, sign up for a free account.

## **Hands-On Exercise: Identifying Bugs and Adding Features**

### Provided Web Page Code

Here is the HTML code for the web page you will be working on:

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>To-Do List</title>
    <style>
      body {
        font-family: Arial, sans-serif;
        background-color: #f4f4f4;
        margin: 0;
        padding: 0;
        display: flex;
        justify-content: center;
        align-items: center;
        height: 100vh;
      }
      .todo-container {
        background: #fff;
        padding: 20px;
        border-radius: 8px;
        box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
        width: 300px;
      }
      h2 {
        margin: 0 0 20px;
        text-align: center;
      }
      ul {
        list-style: none;
        padding: 0;
      }
      ul li {
        background: #f9f9f9;
        margin-bottom: 10px;
        padding: 10px;
        border-radius: 4px;
        display: flex;
        justify-content: space-between;
        align-items: center;
      }
      .task-text {
        flex: 1;
      }
      .btn {
        margin-left: 10px;
        background: #ff6b6b;
        color: #fff;
        border: none;
        padding: 5px 10px;
        border-radius: 4px;
        cursor: pointer;
      }
      .done {
        text-decoration: line-through;
        color: #999;
      }
    </style>
  </head>
  <body>
    <div class="todo-container">
      <h2>To-Do List</h2>
      <ul id="task-list">
        <li>
          <span class="task-text">Task 1</span>
          <button class="btn" onclick="markAsDone(this)">Done</button>
          <button class="btn" onclick="removeTask(this)">Remove</button>
        </li>
        <li>
          <span class="task-text">Task 2</span>
          <button class="btn" onclick="markAsDone(this)">Done</button>
          <button class="btn" onclick="removeTask(this)">Remove</button>
        </li>
        <li>
          <span class="task-text">Task 3</span>
          <button class="btn" onclick="markAsDone(this)">Done</button>
          <button class="btn" onclick="removeTask(this)">Remove</button>
        </li>
      </ul>
      <input type="text" id="new-task" placeholder="Add a new task" />
      <button class="btn" onclick="addTask()">Add Task</button>
    </div>

    <script>
      function markAsDone(button) {
        const taskText = button.parentElement.querySelector(".task-text");
        if (taskText.classList.contains("done")) {
          taskText.classList.remove("done");
        } else {
          taskText.classList.add("error");
        }
      }

      function removeTask(button) {
        const taskItem = button.parentElement;
        taskItem.parentNode.removeChild(taskItem.previousElementSibling);
      }

      function addTask() {
        const taskList = document.getElementById("task-list");
        const newTaskText = document.getElementById("new-task").value;
        const newTask = document.createElement("li");
        newTask.innerHTML = `
                <span class="task-text">${newTaskText}</span>
                <button class="btn" onclick="markAsDone(this)">Done</button>
                <button class="btn" onclick="removeTask(this)">Remove</button>
            `;
        taskList.appendChild(newTask.previousElementSibling);
      }
    </script>
  </body>
</html>
```

### Explanation of the HTML Page

This HTML page is a simple to-do list application where you can add tasks, mark them as done, and remove them. However, there are intentional bugs in the code:

- The application does not properly mark tasks as done.
- The application removes the previous task instead of the selected task.
- The application does not correctly add a new task.

### Setting Up the Web Development Environment

1. **Create the Web Page File:**

   - Open your preferred code editor (e.g., Visual Studio Code).
   - Create a new file and name it `index.html`.
   - Copy the provided HTML code and paste it into the `index.html` file.

2. **Open the Web Page in a Browser:**

   - Save the `index.html` file.
   - Open the file in a web browser by double-clicking it or right-clicking it and selecting "Open with" followed by your preferred browser.
   - Test all functionalities like adding, marking done, and removing tasks, and note any issues.

### Identifying and Fixing Bugs

1. **Upload the Code to ChatGPT:**

   - Use ChatGPT's file upload feature to upload the `index.html` file.

2. **Identify Bugs in the Code:**

   - Ask ChatGPT to identify any bugs in the provided code. Use the prompt: "Can you help me find any issues in this HTML code that might be causing it to not work as expected?"

3. **Fix the Bugs:**

   - ChatGPT will guide you through identifying the bugs. Examples of prompts to use:
     - "Why is the task not being marked as done correctly?"
     - "Why is the wrong task being removed?"
     - "Why is the new task not being added correctly?"

4. **Verify the Fixes:**

   - After following ChatGPT's guidance to fix the bugs, save the changes in your code editor.
   - Refresh the web page in your browser to see if the issues are resolved.

5. **Document Your Findings:**
   - Write down the bugs identified by ChatGPT and the steps taken to fix them.

### Adding a Simple AI-Driven Feature

1. **Choose a Simple Feature:**

   - For this lab, you will add a feature that changes the background color of the page to a random color each time a task is added or removed.

2. **Integrate the Feature:**

   - Use ChatGPT to guide you through adding the AI-driven feature. Use the prompt: "How can I add a feature to change the background color to a random color each time a task is added or removed in my HTML code?"

3. **Verify the Feature:**

   - Save the changes in your code editor.
   - Refresh the web page in your browser to see if the background color changes correctly each time a task is added or removed.

4. **Document Your Findings:**
   - Write down the steps ChatGPT took to help you add the AI-driven feature.
   - Note any challenges faced and how they were resolved.

### Example Workflow:

1. **Identify Bugs:**

   - "Can you help me find any issues in this HTML code that might be causing it to not work as expected?"

2. **Fix Bugs:**

   - "Why is the task not being marked as done correctly?"

3. **Choose a Feature:**

   - "How can I add a feature to change the background color to a random color each time a task is added or removed in my HTML code?"

### Creating a Report

1. **Compile Your Notes:**

   - Compile all the notes you have taken during the lab into a Google Doc.
   - Include the steps ChatGPT took for identifying and fixing bugs, and adding the AI-driven feature.

2. **Include Visual Evidence:**

   - Paste screenshots of the fixed web page and the AI-driven feature into the Google Doc.
   - Write a brief description for each screenshot, explaining the functionality added.
   - Include a screenshot of the final full code.

3. **Answer the Following Questions in Your Report:**
   - What bugs were identified and how were they fixed?
   - What AI-driven feature did you add to the web page?
   - How did ChatGPT assist in identifying bugs, fixing them, and adding the new feature?

### Submission Instructions

- Save your Google Doc with the title "Lab_Web_Development_YourName".
- Make sure the link to your online document is set to public or anyone with the link can view.
- Submit the link to your online document in the provided submission form.

<br />

## **Summary**

In this lab, you used ChatGPT to identify and fix bugs in a web page code, and added a simple AI-driven feature. You learned how to enhance a web application with AI, test and debug the application, and improve user interaction and experience. You also documented your findings and created a comprehensive report.

Congratulations on completing the lab! You have demonstrated your ability to use ChatGPT for web development and AI integration. Continue to explore and apply these skills in your future projects.
