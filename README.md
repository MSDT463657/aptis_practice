Markdown

# 🧠 Aptis Grammar & Vocabulary Practice Test Simulator

An interactive, browser-based simulation of the **Aptis Grammar & Vocabulary Test**, built entirely with HTML, CSS, and JavaScript. This lightweight project lets learners practise grammar and vocabulary in the same format as the official Aptis Core test, with automatic scoring and instant visual feedback.

***

## 📋 Table of Contents

1.  [Overview](#-overview)
2.  [Features](#-features)
3.  [File Structure](#-file-structure)
4.  [Getting Started](#-getting-started)
5.  [Customization](#-customization)
6.  [Technical Notes (Scoring Logic)](#-technical-notes-scoring-logic)
7.  [Future Enhancements](#-future-enhancements)
8.  [Author & License](#-author--license)

***

## 📋 Overview

The Aptis Practice Test Simulator reproduces the two-part structure of the **Aptis Core test**:

* **Grammar Section:** 25 multiple-choice questions on English grammar and structure
* **Vocabulary Section:** 25 multiple-choice questions testing synonyms, collocations, definitions, and contextual usage
* **Total:** **50 questions**
* **Automatic Scoring:** Calculates total score and highlights results after submission

This tool is ideal for practice under **exam-style conditions**.

> ⚠️ **Disclaimer:** This tool is for educational practice only and is **not affiliated with or endorsed by the British Council.**

***

## 🎯 Features

| Feature | Description |
| :--- | :--- |
| ✅ **Authentic Aptis layout** | Two 25-question sections (Grammar & Vocabulary) |
| ⚡ **Automatic scoring** | Calculates total score instantly |
| 🎨 **Color feedback** | **Green** = correct, **Red** = incorrect |
| 💻 **Runs offline** | No server or backend required |
| 📱 **Mobile responsive** | Works on phones, tablets, and desktops |
| 🛠 **Easy to customize** | All code in a single HTML file |

***

## 🧩 File Structure

The project is designed for maximum portability.

aptis-practice/
│ ├── aptis_practice.html # Complete simulator (HTML + CSS + JS)
└── README.md             # This documentation


***

## 🚀 Getting Started

### Clone or Download

```bash
git clone [https://github.com//aptis-practice.git](https://github.com//aptis-practice.git)
cd aptis-practice
Alternatively, download aptis_practice.html directly from GitHub.

Run the Simulator
Open aptis_practice.html in any modern browser (Chrome, Safari, Firefox, etc.).

Take the Test
Answer all 50 questions.

Click Submit Test.

Your total score appears in a popup.

Questions highlight green for correct and red for incorrect.

🌐 Hosting on GitHub Pages
The simulator can be hosted directly:

Go to your repository Settings → Pages.

Select the main branch and / (root) folder.

Click Save.

🧰 Customization
Editing Questions
Each question is contained within a <div class="question" data-answer="..."> block in aptis_practice.html.

Example:

HTML

<div class="question" data-answer="have">
    <p>I ______ never seen such a view before.</p>
    </div>
To set the correct answer, change the data-answer attribute to match the value of one of the radio buttons.

Changing Feedback Colours
Modify the CSS section at the top of the file:

CSS

.correct { background:#E6FFE6; border-left-color:#84BD00; } 
.incorrect { background:#FFE6E6; border-left-color:#D22630; }
🧮 Technical Notes (Scoring Logic)
The core scoring is handled by Vanilla JavaScript:

JavaScript

function gradeTest() {
  let total = 0;
  const questions = document.querySelectorAll('.question');
  
  questions.forEach(q => {
    const correct = q.dataset.answer.trim().toLowerCase();
    const selected = q.querySelector('input[type="radio"]:checked');

    if (selected && selected.value.trim().toLowerCase() === correct) {
      total++;
      q.classList.add('correct');
    } else {
      q.classList.add('incorrect');
    }
  });
  alert(`✅ Test Complete! Your Score: ${total} / ${questions.length}`);
}
📈 Future Enhancements
Potential features to extend the simulator:

⏱ Add a 25-minute countdown timer.

💬 Display correct answers inline after submission.

📤 Export scores to a file (CSV/JSON).

🔀 Randomise question order.

🧾 Add detailed explanations per question.

👤 Author & License
Author
Michael D. Jones Master Trainer & Instructional Designer

AI & Learning Technology Specialist 📧 your.email@example.com | 🌐 yourwebsite.com | 💼 LinkedIn Profile

License
This project is licensed under the MIT License. You may copy, modify, and distribute this project freely for educational or non-commercial use. Attribution is appreciated.

⭐ Support
If you find this simulator helpful, please Star ⭐ the repository!








