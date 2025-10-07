# 🧠 Aptis Grammar & Vocabulary Practice Test Simulator

An interactive, browser-based simulation of the Aptis Grammar & Vocabulary Test, built entirely with HTML, CSS, and JavaScript. This lightweight project lets learners practise grammar and vocabulary in the same format as the official Aptis Core test, with automatic scoring and instant visual feedback.

---

## 📋 Overview

The Aptis Practice Test Simulator reproduces the two-part structure of the Aptis Core test:

- **Grammar Section**: 25 multiple-choice questions on English grammar and structure  
- **Vocabulary Section**: 25 multiple-choice questions testing synonyms, collocations, definitions, and contextual usage  
- **Total**: 50 questions  
- **Automatic Scoring**: Calculates total score and highlights results after submission  

Learners can review their performance immediately, identifying strengths and areas for improvement.

---

## 🎯 Features

| Feature               | Description                                                   |
|-----------------------|---------------------------------------------------------------|
| ✅ Authentic Aptis layout | Two 25-question sections (Grammar & Vocabulary)             |
| ⚡ Automatic scoring   | Calculates total score instantly                             |
| 🎨 Color feedback      | Green = correct, Red = incorrect                             |
| 💻 Runs offline        | No server or backend required                                |
| 📱 Mobile responsive   | Works on phones, tablets, and desktops                       |
| 🛠 Easy to customize   | All code in a single HTML file                               |

---

## 🧩 File Structure

```
aptis-practice/
├── aptis_practice.html   # Complete simulator (HTML + CSS + JS)
└── README.md             # This documentation
```

All styling and logic are contained inside the HTML file for portability.

---

## 🚀 Getting Started

### 1. Clone or Download

```bash
git clone https://github.com/<your-username>/aptis-practice.git
cd aptis-practice
```

Or download `aptis_practice.html` directly from GitHub.

### 2. Run the Simulator

Open `aptis_practice.html` in any modern browser:

- **Windows**: right-click → Open with Chrome  
- **Mac**: double-click or drag into Safari / Chrome  

### 3. Take the Test

1. Answer all 50 questions  
2. Click **Submit Test**  
3. Your total score appears in a popup  
4. Questions highlight green (correct) or red (incorrect)

---

## 🧠 Educational Purpose

This simulator is ideal for:

- Students preparing for Aptis Core (Grammar & Vocabulary)  
- Teachers conducting Aptis preparation courses  
- Trainers delivering English proficiency workshops  
- Self-study learners practising under exam-style conditions  

> ⚠️ This tool is for educational practice only and is not affiliated with or endorsed by the British Council.

---

## 🛠 Customization

### Editing Questions

Each question is defined inside a `<div class="question" data-answer="...">` block.

**Example**:

```html
<div class="question" data-answer="have">
  <p>I ______ never seen such a view before.</p>
  <label><input type="radio" name="q1" value="have"> Have</label>
  <label><input type="radio" name="q1" value="has"> Has</label>
  <label><input type="radio" name="q1" value="had"> Had</label>
</div>
```

Change the `data-answer` attribute to set the correct response.

### Changing Colours

Modify the CSS section at the top of the file:

```css
.correct { background: #E6FFE6; border-left-color: #84BD00; }
.incorrect { background: #FFE6E6; border-left-color: #D22630; }
```

### Adding Features

You can extend functionality by:

- ⏱ Adding a 25-minute countdown timer  
- 🔀 Randomising question order  
- 💬 Showing correct answers inline after submission  
- 📤 Exporting results to CSV or JSON  

---

## 🌐 Hosting on GitHub Pages

1. Push your repository to GitHub  
2. In the repository, go to **Settings → Pages**  
3. Under **Branch**, choose `main` and folder `/ (root)`  
4. Click **Save**

After a short build, your simulator will be live at:

```
https://<your-username>.github.io/aptis-practice/
```

---

## 🧮 Technical Notes

Built with:

- **HTML5** for structure  
- **CSS3** for layout and responsive design  
- **Vanilla JavaScript (ES6)** for interactivity  

### Core Scoring Logic

```javascript
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
```

---

## 📈 Future Enhancements

- ⏱ Add a countdown timer  
- 💬 Display correct answers inline  
- 📤 Export scores to a file  
- 🔀 Randomise question order  
- 🧾 Add detailed explanations per question  

---

## 👤 Author

**Michael D. Jones**  
Master Trainer & Instructional Designer  
Saudi Aramco | AI & Learning Technology Specialist  
📧 your.email@example.com  
🌐 yourwebsite.com  
💼 [LinkedIn Profile](https://www.linkedin.com)

---

## 📜 License

Licensed under the **MIT License**.  
You may copy, modify, and distribute this project freely for educational or non-commercial use.  
Attribution appreciated.

---

## ⭐ Support

If you find this simulator helpful:

- Star ⭐ the repository  
- Fork it and adapt it for your own learners  
- Share it with colleagues preparing for Aptis or English proficiency testing  

Enjoy practising — and best of luck on your Aptis exam!