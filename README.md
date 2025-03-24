# Exam-Quiz-Test Platform

A lightweight, browser-based quiz platform that allows users to create and customize tests by simply editing one HTML file. It includes a tool to convert human-readable questions into JSON format for easy integration. The application is **fully open-source** under the **MIT license**.


![image](https://github.com/user-attachments/assets/3ddddb5a-9f9b-4915-a84b-52cb98bbfdd7)

# DISCORD Server:
On the server anyone can feel free to ask questions, engage in the comunity and discover other free open source software i build
**https://discord.gg/4enDY8yhuS**

## Features

✅ **Customizable Questions & Timer**
- Edit a single HTML file to set the dataset of questions and test duration.

✅ **Single & Multiple Choice Questions**
- Supports both **single-choice** and **multi-choice** question formats.

✅ **Dark Mode & Light Mode**

✅ **Randomized Question & Answer Order**

✅ **Instant Feedback on Mistakes**

✅ **Accurate Scoring System**
- **Single-choice questions:** 100% or 0% per question.
- **Multiple-choice questions:**
  - Correct partial selections get **partial percentage**.
  - Any wrong selection results in **0% for that question**.

✅ **Total Score Calculation**

✅ **No Installation Required**
- The quiz runs **directly in the browser**—no backend or server required.
  
✅ **Separate Question Converter Tool**
- Convert human-readable question formats into JSON format for easy integration.
  
✅ Supports multiline questions using ```<q> and </q>```

✅ Properly extracts code blocks (```)

---

## Usage Instructions

### 1️⃣ **Editing Questions & Timer**
Modify the provided HTML file to:
- Set the total **quiz time**.
- Input your **questions and answers**.

  ```
  /******************************************************
     * 1) CONFIGURATION & QUESTION DATA (inlined)
  ******************************************************/
    const config = {
      // total time in seconds
      totalTime: 90,
      // how many questions to pick
      questionsToPick: 5
    };
  ```

### 2️⃣ **Question Format (Human-Readable)**
This is how to prepare your questions before using the conversion tool to add them to the test

> Number in front indicates start of an question

> Answers need to be below the question

> Questions should not have empty lines below each other in prepared data 

> • for answers is optional, answers can be added without it by being below the question. Program will ignore • if its present it. Everything in the lines below the question is read as answer, this is useful if questions are copied from a PDF

> Everything selected with an * next to it is marked as a correct answer

> To make multichoice question just add * to more answers

> To make a multilined question use ```<q> </q>``` to wrap the question around

> For code containing multilined questions to display in a codeblock use 3 ` on the left and right side of the code

EXAMPLES OF PREPARED DATA FOR CONVERSION:

```txt
1. Choose the right answer to 2+2
• 1
• 2
• 4 *
• 5
2. What of the following are fruits?
• apple *
• banana *
• melon *
• cucumber
3. <q> Multilined question like this
can contain a lot of stuff like
asking about how was your day </q>
• good *  
• bad
• i dont know
• i dont wanna say 
4. <q> What does the following code do

``` function add(a, b) { return a + b; } ```

Select the right answer from below:
</q>
• It subtracts  
• It adds *  
• It multiplies  
• It divides  



```

### 3️⃣ **JSON Converted Format**
```
    const questionPool = [
      {
        question: "Driving in ______ weather is dangerous due to lack of visibility.",
        options: ["freezing", "foggy", "shiny", "rainy"],
        correctAnswers: [1],
        type: "single"
      },
      {
        question: "Which of the following are fruit?",
        options: ["Carrot", "Apple", "Broccoli", "Strawberry", "Lemon"],
        correctAnswers: [1, 3, 4],
        type: "multiple"
      },
      {
        question: "2 + 2 = ?",
        options: ["3", "4", "5", "6"],
        correctAnswers: [1],
        type: "single"
      },
      {
        question: "Select all prime numbers:",
        options: ["2", "3", "4", "8", "11"],
        correctAnswers: [0, 1, 4],
        type: "multiple"
      },
      {
        question: "What color is the sky on a clear day?",
        options: ["Blue", "Green", "Yellow", "Red"],
        correctAnswers: [0],
        type: "single"
      },
      // add more questions if you want ...
    ];
```

### 4️⃣ **Running the Quiz**
Simply open the HTML file in any modern web browser. The quiz will start immediately.

### 5️⃣ **Using the Question Converter Tool**
Navigate to the **Question Converter Page**, paste the human-readable format, and generate JSON to integrate into the quiz.

![image](https://github.com/user-attachments/assets/5b66c834-8760-46f0-a613-127d752f15b5)


---

## Installation (Optional for Local Development)
1. Clone the repository:
   ```sh
   git clone https://github.com/Refloow/Exam-Quiz-Test.git
   ```
2. Open `index.html` in your browser.


## License

This project is **open-source** under the **MIT License**. Feel free to use, modify, and distribute it!


## Contributing
We welcome contributions! Feel free to submit pull requests or report issues.


Enjoy building your quizzes! 🚀
