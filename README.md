# 🤖 Smarty Pinball

A fun, elaborate virtual pinball game featuring the Smarty LLC brand and robot mascot. Built as a self-contained HTML file that can be easily embedded into any website, including Squarespace.

![Smarty Pinball Game](https://github.com/user-attachments/assets/0f02038b-bb07-4fe8-a934-9ecf2d74f46c)

## 🎮 Features

### Core Gameplay
- **Standard Pinball Controls**: Fully functional left and right flippers controlled via keyboard
- **Plunger System**: Launch balls into play with the space bar
- **Realistic Physics**: Custom-built physics engine with gravity, friction, and collision detection
- **3 Lives System**: Start with 3 balls and try to keep them in play

### Scoring System
- **Bumpers**: Hit the robot-adorned bumpers for 100 points each
- **Target Walls**: Strike the cyan target walls for 50 points
- **Bonus Multiplier**: Hit all 3 bumpers in succession to activate a 2x score multiplier
- **High Score Tracking**: Persistent high score saved in browser local storage

### Visual Theme
- **Smarty LLC Branding**: Professional blue gradient color scheme (#1e3c72 to #2a5298)
- **Robot Mascot**: Featured prominently on bumpers and game over screen
- **Modern UI**: Clean, responsive design with glowing effects and smooth animations
- **Live Scoreboard**: Real-time score, high score, and balls remaining display

### Interactive Elements
- **3 Robot Bumpers**: Orange circular bumpers with robot mascots that provide powerful bounces
- **Target Walls**: Cyan-colored walls positioned throughout the table
- **Angled Exit Walls**: Red safety walls at the bottom (though the ball can still escape!)
- **Plunger Lane**: Dedicated launch area with protective wall
- **Responsive Flippers**: Green flippers with smooth animation

## 🕹️ How to Play

### Controls
- **SPACE** - Launch ball from plunger
- **A** or **←** - Activate left flipper
- **D** or **→** - Activate right flipper

### Game Buttons
- **NEW GAME** - Reset and start a fresh game
- **PAUSE** - Pause/unpause the game

### Scoring Strategy
1. Launch the ball with SPACE
2. Use flippers to keep the ball in play
3. Aim for bumpers (100 points each)
4. Hit all 3 bumpers to activate the 2x multiplier
5. Target the cyan walls for additional points (50 each)
6. Keep the ball from falling into the gap between the flippers!

## 🚀 Embedding in Squarespace

### Method 1: Code Block
1. In your Squarespace page editor, add a **Code Block**
2. Copy the entire contents of `index.html`
3. Paste into the code block
4. Save and publish

### Method 2: Custom HTML
1. Upload `index.html` to your Squarespace site files
2. Add an **Embed Block** to your page
3. Use an iframe to embed the game:
```html
<iframe src="/s/index.html" width="640" height="900" frameborder="0"></iframe>
```

### Method 3: Direct Embed
1. Edit the page in Squarespace
2. Add a **Code Block**
3. Paste the HTML file contents directly
4. The game will render inline with your content

## 📁 Files

- **index.html** - Complete self-contained game (HTML + CSS + JavaScript)
- **README.md** - This documentation file

## 🛠️ Technical Details

### Technology Stack
- **Pure Vanilla JavaScript** - No external dependencies
- **HTML5 Canvas** - For rendering the game graphics
- **CSS3** - Modern styling with gradients and animations
- **Local Storage API** - For persistent high score tracking

### Physics Engine
Custom-built physics system featuring:
- Gravity simulation
- Friction and velocity damping
- Circle-to-circle collision detection (ball vs bumpers)
- Rectangle collision detection (ball vs walls and targets)
- Line segment collision detection (ball vs angled walls and flippers)
- Momentum transfer for flipper hits

### Browser Compatibility
Works in all modern browsers that support:
- HTML5 Canvas
- ES6 JavaScript
- CSS3 Gradients
- Local Storage

Tested on:
- Chrome/Edge (Chromium)
- Firefox
- Safari
- Mobile browsers (iOS Safari, Chrome Mobile)

## 🎨 Customization

The game can be easily customized by editing the CSS variables and JavaScript constants in `index.html`:

### Colors
```css
/* Main gradient background */
background: linear-gradient(135deg, #1e3c72 0%, #2a5298 100%);

/* Accent color (borders, score highlights) */
color: #00d4ff;

/* Bumpers */
fillStyle: '#ff6b00'

/* Flippers */
fillStyle: '#00ff00'
```

### Physics
```javascript
this.gravity = 0.4;        // Adjust ball gravity
this.friction = 0.99;      // Adjust ball friction
this.balls = 3;            // Starting number of balls
```

### Scoring
```javascript
const baseScore = 100;     // Points per bumper hit
this.addScore(50);         // Points per target hit
```

## 📱 Responsive Design

The game includes responsive CSS that adapts to different screen sizes:
- Desktop: Full-size experience
- Tablet: Adjusted padding and margins
- Mobile: Optimized layout with smaller text

## 🎯 Future Enhancement Ideas

- Sound effects for bumper hits, ball launch, and flipper activation
- Particle effects for bumper collisions
- Additional table elements (spinners, ramps, bonus zones)
- Multiple ball mode
- Tilt mechanism
- Missions and objectives
- Custom robot mascot graphics (when logo is provided)
- Leaderboard with multiple high scores
- Touch controls for mobile devices
- Background music

## 📄 License

This game was created for Smarty LLC. All rights reserved.

## 🤖 About Smarty LLC

Visit [smartyllc.com](https://smartyllc.com) to learn more about Smarty LLC and their innovative technology solutions.

---

**Enjoy playing Smarty Pinball!** 🎉
