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

**Last Updated**: August 2026
**Status**: ✅ Production Ready

Enjoy playing! 🎮🎉
