# 🎮 Tic-Tac-Toe Game

A fully functional, interactive tic-tac-toe game built with vanilla HTML, CSS, and JavaScript. Play against an intelligent AI opponent with a modern, responsive user interface.

## 📋 Table of Contents

- [Features](#features)
- [Project Structure](#project-structure)
- [Installation](#installation)
- [How to Play](#how-to-play)
- [Game Rules](#game-rules)
- [AI Strategy](#ai-strategy)
- [Customization](#customization)
- [Deployment](#deployment)
- [Browser Support](#browser-support)
- [License](#license)
- [Author](#author)

## ✨ Features

- **AI Opponent**: Smart computer player with strategic decision-making
- **Win Detection**: Automatic detection of wins, losses, and draws
- **Game Statistics**: Track your wins, losses, and draws across multiple games
- **Undo Functionality**: Take back your last move
- **Responsive Design**: Works seamlessly on desktop, tablet, and mobile devices
- **Modern UI**: Beautiful gradient background and smooth animations
- **No Dependencies**: Pure vanilla HTML, CSS, and JavaScript - no external libraries required
- **Local Storage**: All game data stored locally in your browser
- **Instant Play**: Just open the file in a browser - no installation needed

## 📁 Project Structure

```
tictactoe-game/
├── index.html          # Main game file (all-in-one)
└── README.md           # This documentation file
```

## 🚀 Installation

### Option 1: Direct Download & Open
1. Download the `tictactoe.html` file
2. Double-click the file to open it in your default browser
3. Start playing immediately!

### Option 2: From a Web Server
1. Download `tictactoe.html`
2. Place it on your web server
3. Navigate to the file URL in your browser

### Option 3: Local Development
```bash
# Clone or download the repository
git clone <repository-url>
cd tictactoe-game

# Open in your favorite browser
open index.html

# Or use a local server (Python)
python -m http.server 8000

# Or use Node.js
npx http-server
```

## 🎯 How to Play

1. **Start the Game**: Open `tictactoe.html` in your web browser
2. **Make Your Move**: Click any empty cell to place your X
3. **AI Responds**: The computer automatically places an O
4. **Win Conditions**:
   - Get three of your X's in a row (horizontal, vertical, or diagonal) to win
   - Block the computer from getting three O's in a row
   - If all cells are filled with no winner, it's a draw

5. **Game Controls**:
   - **New Game**: Start a fresh game
   - **Undo**: Take back your last move (must have at least 2 moves made)

6. **Track Progress**: View your statistics at the bottom of the screen

## 📜 Game Rules

### Winning Combinations
The following positions win the game:

**Rows:**
- Top: positions 0, 1, 2
- Middle: positions 3, 4, 5
- Bottom: positions 6, 7, 8

**Columns:**
- Left: positions 0, 3, 6
- Center: positions 1, 4, 7
- Right: positions 2, 5, 8

**Diagonals:**
- Top-left to bottom-right: positions 0, 4, 8
- Top-right to bottom-left: positions 2, 4, 6

### Draw
A draw occurs when all 9 cells are filled with no winner (you and the computer cannot complete a winning line).

## 🤖 AI Strategy

The computer opponent uses the following strategy (in order of priority):

1. **Win Move**: If the computer has 2 in a row with an empty cell, it completes the line
2. **Block Player**: If you have 2 in a row with an empty cell, the computer blocks you
3. **Control Center**: Takes the center cell (position 4) if available
4. **Take Corners**: Prefers corner cells (positions 0, 2, 6, 8) for strategic advantage
5. **Fill Remaining**: Takes any available cell if no strategic move exists

This makes the AI challenging but fair - it won't be unbeatable, but it's a worthy opponent!

## 🎨 Customization

### Change Colors

Edit the gradient in the `<style>` section:
```css
background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
```

Try these gradient combinations:
- Sunset: `linear-gradient(135deg, #f093fb 0%, #f5576c 100%)`
- Ocean: `linear-gradient(135deg, #4facfe 0%, #00f2fe 100%)`
- Forest: `linear-gradient(135deg, #43e97b 0%, #38f9d7 100%)`

### Change Button Colors
```css
button {
    border: 2px solid #667eea;  /* Border color */
    color: #667eea;              /* Text color */
}
```

### Modify Game Speed
In the JavaScript section, find this line:
```javascript
setTimeout(() => {
    makeAIMove();
    ...
}, 500);  // Change 500 to adjust AI response time (in milliseconds)
```

### Add Sound Effects
Add audio elements to provide feedback:
```javascript
// Example: Add this when a move is made
const moveSound = new Audio('path-to-sound.mp3');
moveSound.play();
```

## 🌐 Deployment

### 1. **Netlify (Recommended - Easiest)**
```bash
# Visit netlify.com
# Drag and drop tictactoe.html
# Your game is live instantly!
```

### 2. **GitHub Pages**
```bash
# Create a GitHub repository
git init
git add README.md tictactoe.html
git commit -m "Add tic-tac-toe game"
git branch -M main
git remote add origin <your-repository-url>
git push -u origin main

# Enable GitHub Pages in repository settings
# Your game will be available at:
# https://yourusername.github.io/tictactoe/tictactoe.html
```

### 3. **Vercel**
```bash
# Visit vercel.com
# Connect your GitHub account
# Import the repository
# Deploy automatically
```

### 4. **Replit**
1. Go to [replit.com](https://replit.com)
2. Create a new HTML project
3. Copy the contents of `tictactoe.html` into `index.html`
4. Click "Run"
5. Get a shareable public URL

### 5. **Local Server**
```bash
# Using Python 3
python -m http.server 8000

# Using Node.js
npx http-server

# Using PHP
php -S localhost:8000

# Then visit: http://localhost:8000/tictactoe.html
```

## 🌍 Browser Support

This game works on all modern browsers:

| Browser | Support |
|---------|---------|
| Chrome | ✅ Full Support |
| Firefox | ✅ Full Support |
| Safari | ✅ Full Support |
| Edge | ✅ Full Support |
| Opera | ✅ Full Support |
| Internet Explorer | ❌ Not Supported |

## 📱 Mobile Support

The game is fully responsive and works great on:
- ✅ iPhone and iPad
- ✅ Android devices
- ✅ Tablets
- ✅ Desktop computers
- ✅ Tablets

## 🔧 Technical Details

### Architecture
- **Frontend**: Pure HTML5, CSS3, and JavaScript (ES6+)
- **No Backend Required**: Completely client-side
- **No Dependencies**: Zero external libraries
- **File Size**: < 15 KB
- **Performance**: Instant load time

### Key Functions

```javascript
// Check if there's a winner
checkWinner(testBoard)

// Get optimal AI move
getAIMove()

// Update the game board display
updateBoard()

// Handle player clicks
handleCellClick(event)

// Make AI move
makeAIMove()

// Reset the game
resetGame()

// Undo the last move
undoMove()

// Update game status
updateStatus()

// Update statistics
updateStats()
```

### Game State
- `board`: Array of 9 cells (empty string, 'X', or 'O')
- `gameActive`: Boolean indicating if game is in progress
- `isPlayerTurn`: Boolean indicating whose turn it is
- `moveHistory`: Array tracking all moves made
- `stats`: Object tracking wins, losses, and draws

## 🐛 Troubleshooting

**Q: The game won't open**
- A: Make sure you're opening it in a modern web browser (Chrome, Firefox, Safari, Edge)

**Q: The AI plays instantly but I want it slower**
- A: Find the `setTimeout` line and increase the value (e.g., from 500 to 1000)

**Q: I want to reset my statistics**
- A: Open developer tools (F12), go to Console, and clear your browser's local storage

**Q: Can I play on my phone?**
- A: Yes! The game is fully responsive and mobile-friendly

**Q: Can I embed this on my website?**
- A: Yes! You can use an iframe: `<iframe src="tictactoe.html"></iframe>`

## 💡 Enhancement Ideas

Interested in learning game development? Here are some ideas to extend this project:

1. **Difficulty Levels**: Add Easy, Medium, and Hard AI modes
2. **Multiplayer**: Add local multiplayer (player vs player)
3. **Online Multiplayer**: Use WebSockets for real-time multiplayer
4. **Sound Effects**: Add audio feedback for moves and wins
5. **Themes**: Implement dark mode and multiple color themes
6. **Animations**: Add winning line highlight animation
7. **Leaderboard**: Track high scores and best streaks
8. **Game History**: Display replay of previous games
9. **Touch Gestures**: Add swipe controls for mobile
10. **PWA**: Convert to Progressive Web App for offline play

## 📄 License

This project is open source and available under the MIT License. Feel free to use, modify, and distribute this code for personal or commercial projects.

## 👨‍💻 Author

Created as an educational project for learning game development with vanilla JavaScript.

## 🤝 Contributing

Contributions are welcome! If you'd like to improve this project:

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## 📞 Support

If you have questions or issues:
- Check the Troubleshooting section above
- Review the code comments
- Test in a different browser
- Clear your browser cache

## 🎓 Learning Resources

Want to learn more about game development?

- [MDN Web Docs - Game Development](https://developer.mozilla.org/en-US/docs/Games)
- [JavaScript.info - Game Loop](https://javascript.info/)
- [CSS Tricks - Game Development](https://css-tricks.com/)
- [Codecademy - JavaScript Games](https://www.codecademy.com/)

## ⭐ If You Enjoyed This

If you found this project helpful:
- Star this repository
- Share it with others
- Consider contributing improvements
- Use it as a learning resource

## 📈 Version History

### Version 1.0.0 (Initial Release)
- Core game mechanics
- AI opponent with strategy
- Win/draw detection
- Game statistics
- Responsive design
- Undo functionality

---

**Last Updated**: August 2026
**Status**: ✅ Production Ready

Enjoy playing! 🎮🎉
