# WEB2020_shooting_targets
Create a game to shoot targets using JavaScript timers

## Create the HTML code
Create a new file "game.html" and type the following code inside.

```html
<!DOCTYPE html>
<html>
	<head>
		<title>Shooting Target</title>
	</head>
	<body>
		<script type="text/javascript">
			// your javascript code here
		</script>
	</body>
</html>
```

## Add the target
Type the following code in the <script> section. This code will make the background pink, add a target image from the internet and resize it to 100px. Save and see what happens.

```javascript
var body = document.getElementsByTagName('body')[0];
body.innerHTML="Hola Mundo";
body.style="background-color:pink;";

var img = new Image();
img.src = 'http://aws.canequity.com/assets/images/target.png';
body.appendChild(img);

img.style.width="100px"
img.style.position="absolute";
```

## Start moving the target
Type the following code in the <script> section, right after the code from before. This code will make the target image to move. Save and see what happens.

```javascript
setInterval(function(){
	var posH = Math.random() * window.innerWidth;
	var posV = Math.random() * window.innerHeight;

	img.style.top = posV + "px";
	img.style.left = posH + "px";
}, 1000);

```

## Add the score
Type the following code in the <script> section, right after the code from before. This code will add a scoreboard, but still nothing will happen when you click the target. Save and see what happens.

```javascript
var score = 0;
var board = document.createTextNode(score);
body.appendChild(board);
```

## Make the target clickeable
Type the following code in the <script> section, right after the code from before. This code will add one to the scoreboard once the target is clicked. There are still issues, like the target won't dissapear when you click on it. Save and see what happens.

```javascript
img.onclick = function () {
	score = score + 1;
	board.nodeValue = score;
}
```

# What else can we do?
Can you make the following improvements to this game? If you get lost check at the code example "game.html".
1. How can we ensure the target never goes out of the screen?
2. Can we make the target disappear when is clicked?
3. How to make the target go faster every time you click?
4. How to make each target's size be different?
5. Can we add a winning condition to your game?

# Take it to the next level
If you still want more challenge, do the following improvements:
1. Add a cool background image to the game and improve the way points look.
2. Show a nicer winning message with a retry button.
3. Add a nice animation to the target when you hit on it.
4. Get two points when you click a target smaller than 50px.
5. If not hit, make the target to move over the screen instead of disappearing and appearing
6. Make the screen blink red when you hit the target.
7. Add a losing condition when the player spend over 2 minutes playing.
8. Make three different targets appear on the screen at the same time.
9. Add a shooting sound when you click.
10. Add a break sound when you hit the target.
11. Animate so when you click the target, a small and round projectile moves rapidly from the center of the screen to the center of the target.

