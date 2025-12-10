# The React Quiz 🎯

An interactive quiz application built with React to test your React knowledge. Features a timed quiz system with score tracking and a clean, modern UI.

![React Quiz](https://img.shields.io/badge/React-19.0.0-blue)
![License](https://img.shields.io/badge/license-MIT-green)

![Quiz App Banner](./Banar_Quiz_App.png)

## 🌟 Features

- **15 React Questions** covering fundamental to advanced concepts
- **Timer System** - 30 seconds per question
- **Score Tracking** - Real-time points calculation
- **High Score** - Keeps track of your best performance
- **Progress Bar** - Visual feedback on quiz completion
- **Instant Feedback** - See correct/incorrect answers immediately
- **Responsive Design** - Works on all devices

## 🚀 Demo

Check out the live demo: [React Quiz App](https://MomenAshraf5.github.io/React-Quiz-App)

## 📸 Screenshots

### Start Screen
The welcome screen shows the total number of questions before starting.

### Quiz Interface
- Question display with multiple choice options
- Timer countdown
- Progress tracker showing current question and points
- Next button to move forward

### Results Screen
- Final score with percentage
- Emoji feedback based on performance
- High score display
- Restart option

## 🛠️ Technologies Used

- **React 19** - UI library
- **useReducer** - State management
- **JSON Server** - Mock API for questions
- **CSS3** - Styling
- **Create React App** - Project setup

## 📋 Prerequisites

Before running this project, make sure you have:

- Node.js (v14 or higher)
- npm or yarn package manager

## ⚙️ Installation

1. Clone the repository
```bash
git clone https://github.com/MomenAshraf5/React-Quiz-App.git
```

2. Navigate to project directory
```bash
cd React-Quiz-App
```

3. Install dependencies
```bash
npm install
```

4. Start the development server
```bash
npm start
```

The app will open at [http://localhost:3000](http://localhost:3000)

## 🎮 How to Use

1. Click **"Let's start"** to begin the quiz
2. Select your answer for each question
3. Click **"Next"** to proceed to the next question
4. Complete all 15 questions before time runs out
5. View your final score and compare with your high score
6. Click **"Restart Quiz"** to try again

## 📁 Project Structure

```
react-quiz/
├── public/
│   ├── questions.json      # Quiz questions data
│   └── logo512.png         # React logo
├── src/
│   ├── components/
│   │   ├── App.js          # Main component with useReducer logic
│   │   ├── Header.js       # App header
│   │   ├── Main.js         # Main content wrapper
│   │   ├── Loader.js       # Loading spinner
│   │   ├── Error.js        # Error display
│   │   ├── StartScreen.js  # Welcome screen
│   │   ├── Question.js     # Question display
│   │   ├── Options.js      # Answer options
│   │   ├── Progress.js     # Progress bar
│   │   ├── Timer.js        # Countdown timer
│   │   ├── NextButton.js   # Navigation button
│   │   ├── FinishScreen.js # Results screen
│   │   └── Footer.js       # Footer wrapper
│   ├── index.css           # Global styles
│   └── index.js            # App entry point
└── package.json
```

## 🎨 Key Features Explained

### State Management
The app uses `useReducer` for complex state management with actions:
- `dataReceived` - Load questions
- `start` - Begin quiz
- `newAnswer` - Record answer and calculate points
- `nextQuestion` - Move to next question
- `finish` - End quiz and update high score
- `restart` - Reset quiz
- `tick` - Update timer

### Timer System
- 30 seconds per question (450 seconds total for 15 questions)
- Automatically finishes quiz when time expires
- Uses `useEffect` with `setInterval` for countdown

### Scoring
- Each question has point values (10-30 points)
- Maximum possible score: 280 points
- High score persists during session

## 🔧 Customization

### Adding/Editing Questions
Edit `public/questions.json`:

```json
{
  "question": "Your question here?",
  "options": ["Option 1", "Option 2", "Option 3", "Option 4"],
  "correctOption": 0,
  "points": 10
}
```

### Changing Timer Duration
In `App.js`, modify:
```javascript
const Secs_per_Question = 30; // Change to desired seconds
```

### Styling
Customize colors in `index.css`:
```css
:root {
  --color-darkest: #343a40;
  --color-theme: #1098ad;
  --color-accent: #ffa94d;
}
```

## 📦 Available Scripts

```bash
npm start        # Run development server
npm test         # Run tests
npm run build    # Build for production
npm run deploy   # Deploy to GitHub Pages
npm run server   # Run JSON server (port 8000)
```

## 🌐 Deployment

This project is configured for GitHub Pages deployment:

```bash
npm run deploy
```

The app will be deployed to: `https://yourusername.github.io/React-Quiz-App`

## 🤝 Contributing

Contributions are welcome! Feel free to:

1. Fork the project
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## 📝 License

This project is open source and available under the MIT License.

## 👨‍💻 Author

**Momen Ashraf**

- GitHub: [@MomenAshraf5](https://github.com/MomenAshraf5)

## 🙏 Acknowledgments

- Created with [Create React App](https://create-react-app.dev/)
- React logo from official React assets
- Loader animation from [CSS Loaders](https://dev.to/afif/i-made-100-css-loaders-for-your-next-project-4eje)

---

⭐ If you found this project helpful, please give it a star!
