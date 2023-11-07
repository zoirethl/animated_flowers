# Heart Beating Animation

This project is a simple web-based heart beating animation created using HTML and CSS. It features a heart-shaped element that pulsates to simulate a heartbeat. Below you'll find the CSS code that creates the animation.

![Heart Beating Animation](Nov-07-2023%2015-11-58.gif)

## Live Preview

You can view a live preview of this heart beating animation by clicking on the following link: [Live Preview](https://zoirethl.github.io/animated_flowers/)


```css
body {
  margin: 0;
  padding: 0;
  display: flex;
  justify-content: center;
  align-items: center;
  min-height: 100vh;
  background-color: #000;
}

.heart {
  width: 100px;
  height: 90px;
  position: relative;
  transform: rotate(-45deg);
  animation: heartbeat 1s ease-in-out infinite;
}

.heart::before,
.heart::after {
  content: '';
  position: absolute;
  top: 0;
  width: 52px;
  height: 80px;
  background: red;
  border-radius: 50px 50px 0 0;
}

.heart::before {
  left: 50px;
  transform: rotate(-45deg);
  transform-origin: 0 100%;
}

.heart::after {
  left: 0;
  transform: rotate(45deg);
  transform-origin: 100% 100%;
}

@keyframes heartbeat {
  0% {
    transform: scale(1);
  }
  50% {
    transform: scale(1.2);
  }
  100% {
    transform: scale(1);
  }
}
```


