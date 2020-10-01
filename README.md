# Piano-kit
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>JS Piano Kit</title>
  <link rel="stylesheet" href="C:\Users\This-PC\Desktop\New WP\JS\DRUMLIT.css">
</head>
<body>

  <! -- Sg Piano Kit-->
  <div class="keys">
    <div data-key="65" class="key">
      <kbd>A</kbd>
      <span class="sound">P65</span>
    </div>
		<div data-key="81" class="key">
			<kbd>Q</kbd>
			<span class="sound">P81</span>
		</div>
    <div data-key="83" class="key">
      <kbd>S</kbd>
      <span class="sound">P83</span>
    </div>
    <div data-key="68" class="key">
      <kbd>D</kbd>
      <span class="sound">P68</span>
    </div>
    <div data-key="70" class="key">
      <kbd>F</kbd>
      <span class="sound">P70</span>
    </div>
    <div data-key="71" class="key">
      <kbd>G</kbd>
      <span class="sound">P71</span>
    </div>
    <div data-key="72" class="key">
      <kbd>H</kbd>
      <span class="sound">P72</span>
    </div>
    <div data-key="86" class="key">
			<kbd>V</kbd>
			<span class="sound">P86</span>
		</div>
    <div data-key="75" class="key">
			<kbd>K</kbd>
			<span class="sound">P75</span>
		</div>
    <div data-key="77" class="key">
			<kbd>M</kbd>
			<span class="sound">P77</span>
		</div>
    <div data-key="85" class="key">
			<kbd>U</kbd>
			<span class="sound">P85</span>
		</div>
    <div data-key="74" class="key">
			<kbd>J</kbd>
			<span class="sound">P74</span>
		</div>
    <div data-key="79" class="key">
			<kbd>O</kbd>
			<span class="sound">P79</span>
		</div>
    <div data-key="89" class="key">
			<kbd>Y</kbd>
			<span class="sound">P89</span>
		</div>
    <div data-key="76" class="key">
			<kbd>L</kbd>
			<span class="sound">P76</span>
		</div>
    <div data-key="80" class="key">
			<kbd>P</kbd>
			<span class="sound">P80</span>
		</div>
    <div data-key="186" class="key">
			<kbd>;</kbd>
			<span class="sound">P186</span>
		</div>


  </div>
    <audio data-key="65" src="http://carolinegabriel.com/demo/js-keyboard/sounds/040.wav"></audio>
    <audio data-key="81" src="http://carolinegabriel.com/demo/js-keyboard/sounds/041.wav"></audio>
    <audio data-key="83" src="http://carolinegabriel.com/demo/js-keyboard/sounds/042.wav"></audio>
    <audio data-key="68" src="http://carolinegabriel.com/demo/js-keyboard/sounds/043.wav"></audio>
    <audio data-key="70" src="http://carolinegabriel.com/demo/js-keyboard/sounds/044.wav"></audio>
    <audio data-key="71" src="C:\Users\This-PC\Desktop\New WP\JS\1, A=Single-clap-sound effect.mp3"></audio>
    <audio data-key="72" src="http://carolinegabriel.com/demo/js-keyboard/sounds/046.wav"></audio>
    <audio data-key="86" src="http://carolinegabriel.com/demo/js-keyboard/sounds/047.wav"></audio>
    <audio data-key="75" src="http://carolinegabriel.com/demo/js-keyboard/sounds/048.wav"></audio>
    <audio data-key="77" src="http://carolinegabriel.com/demo/js-keyboard/sounds/049.wav"></audio>
    <audio data-key="85" src="http://carolinegabriel.com/demo/js-keyboard/sounds/050.wav"></audio>
    <audio data-key="74" src="C:\Users\This-PC\Desktop\New WP\JS\Hit.mp3"></audio>
    <audio data-key="79" src="http://carolinegabriel.com/demo/js-keyboard/sounds/052.wav"></audio>
    <audio data-key="89" src="http://carolinegabriel.com/demo/js-keyboard/sounds/053.wav"></audio>
    <audio data-key="76" src="http://carolinegabriel.com/demo/js-keyboard/sounds/054.wav"></audio>
    <audio data-key="80" src="http://carolinegabriel.com/demo/js-keyboard/sounds/055.wav"></audio>
    <audio data-key="186" src="http://carolinegabriel.com/demo/js-keyboard/sounds/056.wav"></audio>


<script>
  function removeTransition(e) {
    if (e.propertyName !== 'transform') return;
    e.target.classList.remove('playing');
  }

  function playSound(e) {
    const audio = document.querySelector(`audio[data-key="${e.keyCode}"]`);
    const key = document.querySelector(`div[data-key="${e.keyCode}"]`);
    if (!audio) return;

    key.classList.add('playing');
    audio.currentTime = 0;
    audio.play();
  }

  const keys = Array.from(document.querySelectorAll('.key'));
  keys.forEach(key => key.addEventListener('transitionend', removeTransition));
  window.addEventListener('keydown', playSound);
</script>


</body>
</html>
