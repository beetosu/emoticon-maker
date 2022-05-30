<script>
	let emoticon = '(◕‿◕ )';
	
	let isHovered = false;
	let titleEmoticon = isHovered ? '( ◕‿◕)' : '( ◡‿◡)';
	function changeHoverStatus() { isHovered = !isHovered; }

  export default {
    data() {
      return {
        emoticon: '(◕‿◕ )',
	      titleEmoticon: '( ◡‿◡)'
      }
    }
  }
</script>

<style>
  @import url('assets/base.css');

	button.selection {
    border: 0;
		border-radius: 4px;
		width: 7.5rem;
		font-size: 16px;
	}

	button.options {
		border: 0;
		background-color: #82D2EC;
		border-radius: 4px;		
	}

  button:focus {
    border: 2px;
  }

	button:hover:not(:focus) {
		transition: .25s;
	}

	.body {
		background-color: #CCBFE9;
		border-color: #CCBFE9;
	}
	.body:hover {
		background-color: #B1A7C7;
	}

	.eyes {
		background-color: #B8E9E4;	
	}
	.eyes:hover {
		background-color: #A0CAC6;
	}

	.mouth {
		background-color: #FFF8C2;	
	}
	.mouth:hover {
		background-color: #AEAA86;
	}

	.arms {
		background-color: #FFD3CC;
	}
	.arms:hover {
		background-color: #C5A09A;
	}

	.features {
		background-color: #CFF3CA;
	}
	.features:hover {
		background-color: #8FB38A;
	}

	.accessories {
		background-color: #FFE4CC;
	}
	.accessories:hover {
		background-color: #C3B3A4;
	}

	.emoticon input[type="text"] {
		color: #333;
		text-align: center;
	}

	footer a {
		color: #626262;
	}
</style>

<template>
	<header>
		<h1 
			class="title"
			@mouseover="titleEmoticon='( ◕‿◕)'"
			@mouseleave="titleEmoticon='( ◡‿◡)'"
		>
			{{titleEmoticon}} Emoticon Maker
		</h1>	
	</header>
	<section class="buttons" name="buttons">
		<button class="selection body" aria-label="Modify Body">
			Body <br>
			ʕ◕‿◕ ʔ
		</button>
		<button class="selection eyes" aria-label="Modify Eyes">
			Eyes <br>
			(ㆆ‿ㆆ )
		</button>
		<button class="selection mouth" aria-label="Modify Mouth/Nose">
			Nose/Mouth <br>
			(◕益◕ )
		</button>
		<button class="selection arms" aria-label="Modify/Enable Arms">
			Arms <br>
			＼(◕‿◕ )ノ
		</button>
		<button class="selection features" aria-label="Modify/Add Facial Features">
			Features <br>
			(´｡◕‿◕｡`)
		</button>
		<button class="selection accessories" aria-label="Modify/Add Facial Accessories">
			Accessories <br>
			☆(◕‿◕ )♡
		</button>
	</section>
	<section class="emoticon">
		<div class="result">
			<input aria-label="Generated Emoticon" disabled type="text" :value="emoticon" />
			<button class="options" aria-label="Copy">Copy</button>
		</div>
		<div class="options">
			<button class="options" aria-label="Randomize">🎲 Randomize</button>
			<button class="options" aria-label="Share">Share</button>
		</div>
	</section>
	<footer>
		<a href="https://cwalsh.dev">cwalsh.dev</a> |
		<a href="https://twitter.com/beetosu">@beetosu</a> |
		<a href="https://github.com/beetosu/emoticon-maker">Source Code</a> |
		<a href="mailto:me@cwalsh.dev">Contact</a>
	</footer>
</template>