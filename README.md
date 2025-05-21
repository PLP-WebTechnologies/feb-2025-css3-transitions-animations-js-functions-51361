# CSS3 Transitions, Animations, and Advanced JavaScript Functions

## Objectives

Create smooth CSS transitions and animations.
Use JavaScript functions for dynamic behavior.
Implement local storage for data persistence.

## Instructions
Add CSS animations to elements like buttons or images.

>[!NOTE]
> - Write a JavaScript function that:
> - Stores and retrieves user preferences using localStorage.
> - Implements an animation triggered by user actions.

## Tasks

Create a CSS animation.
Store data in localStorage.
Apply JavaScript to trigger animations.

<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Interactive Animation</title>
  <link rel="stylesheet" href="styles.css">
</head>
<body>
  <div class="ball" id="ball"></div>
  <button id="toggleBtn">Toggle Animation</button>
  <button id="resetBtn">Reset Storage</button>

  <script src="script.js"></script>
</body>
</html>





// DOM Elements
const ball = document.getElementById('ball');
const toggleBtn = document.getElementById('toggleBtn');
const resetBtn = document.getElementById('resetBtn');

// Check localStorage for saved state
const savedState = localStorage.getItem('ballAnimation');
if (savedState === 'active') {
  ball.classList.add('bounce-animation');
}

// Toggle Animation
toggleBtn.addEventListener('click', () => {
  ball.classList.toggle('bounce-animation');
  
  // Save state to localStorage
  const isActive = ball.classList.contains('bounce-animation');
  localStorage.setItem('ballAnimation', isActive ? 'active' : 'inactive');
});

// Reset Storage
resetBtn.addEventListener('click', () => {
  localStorage.removeItem('ballAnimation');
  ball.classList.remove('bounce-animation');
});










Happy Coding! 💻✨
