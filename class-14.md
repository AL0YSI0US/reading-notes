# Code 201 Reading Notes

## Class 14

[Class 1 Instructor's Repo](https://github.com/codefellows/seattle-201n21/tree/master/class-01)

[<== Previous Lesson](class-13.md) [Next Lesson ==>](class-15.md)

[<== Home](README.md) 🏠

## CSS Transforms, Transitions, and Animations

## [CSS Transforms](http://learn.shayhowe.com/advanced-html-css/css-transforms/)

### 2D Rotate

The `transform` property accepts a handful of different values. The rotate value provides the ability to rotate an element from 0 to 360 degrees. Using a positive value will rotate an element clockwise, and using a negative value will rotate the element counterclockwise. The default point of rotation is the center of the element, 50% 50%, both horizontally and vertically. Later we will discuss how you can change this default point of rotation.

**HTML**

````html
<figure class="box-1">`Box 1</figure>
<figure class="box-2">`Box 2</figure>
````

**CSS**

````css
.box-1 {
transform: rotate(20deg);
}
.box-2 {
transform: rotate(-55deg);
}
````

#### .........[play with this code on codepen](https://codepen.io/shayhowe/pen/AKDIp)

Lots of other elements to consider...

+ Rotate
+ Scale
+ tranlsate
+ skew
+ perspective....................etc.

## [CSS Transitions &amp; Animations](http://learn.shayhowe.com/advanced-html-css/transitions-animations/)

For a [transition](http://www.alistapart.com/articles/understanding-css3-transitions/) to take place, an element must have a change in state, and different styles must be identified for each state. The easiest way for determining styles for different states is by using the `:hover`, `:focus`, `:active`, and `:target` pseudo-classes.

There are four transition related properties in total, including `transition-property`, `transition-duration`, `transition-timing-function`, and `transition-delay`. Not all of these are required to build a transition, with the first three are the most popular.

**Transitional Properties**

It is important to note, **not all properties may be transitioned**, only properties that have an identifiable halfway point. Colors, font sizes, and the alike may be transitioned from one value to another as they have recognizable values in-between one another. The `display` property, for example, may not be transitioned as it does not have any midpoint. A handful of the more popular transitional properties include the following.

* `background-color`
* `background-position`
* `border-color`
* `border-width`
* `border-spacing`
* `bottom`
* `clip`
* `color`
* `crop`
* `font-size`
* `font-weight`
* `height`
* `left`
* `letter-spacing`
* `line-height`
* `margin`
* `max-height`
* `max-width`
* `min-height`
* `min-width`
* `opacity`
* `outline-color`
* `outline-offset`
* `outline-width`
* `padding`
* `right`
* `text-indent`
* `text-shadow`
* `top`
* `vertical-align`
* `visibility`
* `width`
* `word-spacing`
* `z-index`

## [8 simple CSS3 transitions that will wow your users](http://www.webdesignerdepot.com/2014/05/8-simple-css3-transitions-that-will-wow-your-users)

1.
2.
3.
4.
5.
6.
7.
8. Why are we writing CSS into HTML? I'll circle back.

## [6 Buttons animated](https://codepen.io/retyui/pen/ByoaXV)

> //author: https://dribbble.com/shots/1527712-Buttons

````HTML
<div class="group">
		<button class="blam">Aloysious</button>
		<button style="-webkit-animation-delay: .3s;animation-delay: .3s;" class="syke">does thier</button>
		<button style="-webkit-animation-delay: .6s;animation-delay: .6s;" class="later">homework</button>
	</div>
```
````

````css
@import url(https://fonts.googleapis.com/css?family=Droid+Sans:700);
		*{
			margin: 0;
			padding: 0;
			box-sizing: border-box;
			transition: all .1s;
		}
		body{
		background-color: #424242;
			font-family: 'Droid Sans', sans-serif;
		}
		.group{
			text-align: center;
			margin: 20px auto;
		}
		.group button{
			margin-top: 10px;
		}
		button{
/*			box-sizing: border-box;*/
			background: NONE;
			border: none;
			outline: none;
			border-radius: 3px;
			padding: 15px 70px;
			color:white;
			text-transform: uppercase;
			font-weight: 700;
			text-shadow: 0 1px 3px rgba(0, 0, 0, 0.41);
			box-shadow: 0 3px 0 0 #383838;
			border:3px solid transparent;
	

			animation: pulse 1s linear infinite alternate;
			-webkit-animation: pulse 1s linear infinite alternate;
		}
		.active,
		button:active{
			background-image: linear-gradient(rgba(0,0,0,.1) 13%, transparent 13%,transparent);
			box-shadow: 0 1px 0 0 #383838;
			color: rgba(0, 0, 0,.45);
			text-shadow: none;
	
	
			-webkit-animation-play-state: paused; 
    	animation-play-state: paused;
		}
		button:focus,
		button:hover{
			-webkit-animation-play-state: paused; 
    	animation-play-state: paused;
		}


		.blam:focus,
		.blam:hover{
			background-color:#0097bd;
		}
		.blam{
			background-color:#00bff0;
			border-color: #00bff0;
		}

		.syke:focus,
		.syke:hover{
			background-color:#ad4e4e;
		}
		.syke{
			background-color:#e06464;
			border-color:#e06464;
		}

		.later:focus,
		.later:hover{
			background-color:#7c8b8f;
		}
		.later{
			background-color:#a8bdc2;
			border-color:#a8bdc2;
		}

		@-webkit-keyframes pulse {
			100% {
				transform: translateY(6.9px); 
			} 
		}

		@keyframes pulse {
			100% {
				transform: translateY(6.9px); 
			} 
		}
````

## [CSS3 Animations: Keyframes](http://codepen.io/akshaychauhan/pen/oAfae)

````HTML
<!-- 
╢╢╢╢╢╢╢╢╢╢╢╢╢╢╢╢╢╢╢╢╢╢╢╢╢╢╢╢╢╢╢╢╢╢╢╢╢╢╢╢╢╢╢╢╢╢╢╢╢╢╢╢╢╢╢╢╢╢╢╢╢╢╢╢╢╢╢╢╢╢╢╢╢╢╢╢╢╢╢╢
░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░
░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░^ ╠░░░░░░░░░░░░┘ ╞░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░
░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░  ╒╢░░░░░░░░░░░┘ ╒╣░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░
░░░░░░░░░░░░░░░░░░░░░░░░░░░░░` ╒░░░░░░Θ┴╚░░░┘  ╢░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░
░░░░░░░░░░░░░░░░░░╢╜`     ║░`     ╢░╣┘  ╪░░┘     ╢░δ┘      ╢░╨ ╞░░░┘ ║░░░░░░░░░░
░░░░░░░░░░░░░░░░░┘  ô╣Θ  ó░┘ ╒╝╜  ╢┘   ╘░╢┘  ╒┘  ╝` ╒╢░┘  ╢╢^ ó░░╢  ╪░░░░░░░░░░░
░░░░░░░░░░░╨╙╜░╢   ╣░╜  ╪╜    ╒ô╪╨  ╪╕      ╢┘  ╧  ╞░╢┘  ╢╜  ╢░╣┘ ╔╣░░░░░░░░░░░░
░░░░░░░░░░╢ ╚Å` ⌐       ,  ╒╖ `` ²  "  ╒   ╢╢             ╒  `² ²╧ ╢░░░░░░░░░░░░
░░░░░░░░░░░╢╪ô╪╢░╢╪╪╢░╢░░╪╪░░╢╪╪╣░╢╪╪╢░░╢╪╢░░╢╪╢░░╢╪╢╢╢╪╪░░╢ô` `╓ô╢░░░░░░░░░░░░░
░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░╝╜` «╪╢░░░░░░░░░░░░░░░░
░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░╜ ╔ô`,╢░░░░░░░░░░░░░░░░░░░
░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░² Å` ô░░░░░░░░░░░░░░░░░░░░░
░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░╗-╤ô░░░░░░░░░░░░░░░░░░░░░░░
░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░

-->


<h1>CSS3 Animations: Keyframes</h1>


<div class="exampleDiv">
  <div class="ball" style="-webkit-animation: bouncing 2s 15 linear;-moz-animation: bouncing 2s 15 linear;"></div>
</div>


<!-- WhatsHelp.io widget -->
<script type="text/javascript">
    (function () {
        var options = {
            facebook: "220186546416", // Facebook page ID
            company_logo_url: "//storage.whatshelp.io/widget/d2/d2db/d2dbaa07f22d96b7ad8426beb00493d0/20031613_10154783116346417_1007255058190022230_n.png", // URL of company logo (png, jpg, gif)
            greeting_message: "Hello, how may I help you? Just send us a message now to get assistance.", // Text of greeting message
            call_to_action: "Message me", // Call to action
            position: "right", // Position may be 'right' or 'left'
        };
        var proto = document.location.protocol, host = "whatshelp.io", url = proto + "//static." + host;
        var s = document.createElement('script'); s.type = 'text/javascript'; s.async = true; s.src = url + '/widget-send-button/js/init.js';
        s.onload = function () { WhWidgetSendButton.init(host, proto, options); };
        var x = document.getElementsByTagName('script')[0]; x.parentNode.insertBefore(s, x);
    })();
</script>
````

```css
@import url(https://fonts.googleapis.com/css?family=Montserrat:700);
body {
  background-color: #ffcc46;
}

::-webkit-scrollbar {
    width: 8px;
}

::-webkit-scrollbar-thumb {
    background: rgba(0,0,0,0.12);
}

::-webkit-scrollbar-track {
    visibility: hidden;
}

h1 {
  font-family: 'Montserrat', helvetica, arial;
  sans-serif;
  margin: 20px;
}

.exampleDiv {
  height: 200px;
  width: 200px;
  border: 1px solid rgba(0, 0, 0, 0.1);
  float: left;
  margin: 20px;
  text-align: center;
  position: relative;
  background-color: #ffffff;
  border-radius: 4px;
}

.ball {
  position: absolute;
  height: 20px;
  width: 20px;
  border-radius: 10px;
  background-color: #c0392b;
}

@-webkit-keyframes bouncing {
  40%, 70%, 90% {
    bottom: 0;
    -webkit-animation-timing-function: ease-out;
  }
  0% {
    bottom: 200px;
    left: 0;
    -webkit-animation-timing-function: ease-in;
  }
  55% {
    bottom: 50px;
    -webkit-animation-timing-function: ease-in;
  }
  80% {
    bottom: 25px;
    -webkit-animation-timing-function: ease-in;
  }
  95% {
    bottom: 10px;
    -webkit-animation-timing-function: ease-out;
  }
  100% {
    left: 110px;
    bottom: 0;
    -webkit-animation-timing-function: ease-out;
  }
  @-moz-keyframes bouncing {
    40%, 70%, 90% {
      bottom: 0;
      -webkit-animation-timing-function: ease-out;
    }
    0% {
      bottom: 200px;
      left: 0;
      -webkit-animation-timing-function: ease-in;
    }
    55% {
      bottom: 50px;
      -webkit-animation-timing-function: ease-in;
    }
    80% {
      bottom: 25px;
      -webkit-animation-timing-function: ease-in;
    }
    95% {
      bottom: 10px;
      -webkit-animation-timing-function: ease-out;
    }
    100% {
      left: 110px;
      bottom: 0;
      -webkit-animation-timing-function: ease-out;
    }
```

## [404](http://codepen.io/kieranfivestars/pen/MYdQxX)...okay that was rad!

````HTML
<h1>B</h1>
<h1>L</h1>
<h1>M</h1>
````

````css
body {
  margin:0;
  font-family:sans-serif;
  color:#f25252;
  background:#f7f7f7;
}
h1 {
  font-size:11rem;
  position:absolute;
  transform:translate(-50%,-50%);
  margin:0;
}
h1:nth-of-type(1){
  animation: range 4s infinite;
}
h1:nth-of-type(2){
  left:50%;
  top:50%;
  animation: size 4s infinite;
}
h1:nth-of-type(3){
  animation: range2 4s infinite;
}
@keyframes range {
  0%  {left:42%;top:50%;font-size:11rem;}
  25% {left:50%;top:40%;font-size:4.5rem;}
  50% {left:58%;top:50%;font-size:11rem;}
  75% {left:50%;top:60%;font-size:4.5rem;}
  100%{left:42%;top:50%;font-size:11rem;}
}
@keyframes range2 {
  0%  {left:58%;top:50%;font-size:11rem;}
  25% {left:50%;top:60%;font-size:4.5rem;}
  50% {left:42%;top:50%;font-size:11rem;}
  75% {left:50%;top:40%;font-size:4.5rem;}
  100%{left:58%;top:50%;font-size:11rem;}
}
@keyframes size {
  0%  {font-size:11rem;}
  25% {font-size:26rem;}
  50% {font-size:11rem;}
  75% {font-size:26rem;}
  100%{font-size:11rem;}
}
````

## [Pure CSS Bounce Animation](http://codepen.io/dp_lewis/pen/gCfBv) whoa!

````HTML
	<div class="animation animation-1">
		<div class="ball"></div>
	</div>
	<div class="animation animation-2">
		<div class="ball"></div>
	</div>
	<div class="animation animation-3">
		<div class="ball"></div>
	</div>
````

````css
/* Animation -------------------- */

@keyframes balltransform {
	0% {
		border-radius:50%;
		height:100%;
		width:60%;
	}
	29% {
		height:100%;
		width:60%;
	}
	30% {
		height:50%;
		width:100%;
	}
	40% {
		height:80%;
		width:80%;
	}
	59% {
		height:100%;
		width:60%;
	}
	60% {
		height:50%;
		width:100%;
		border-radius:50%;
		transform:rotate(0);
	}
	100% {
		height:80%;
		width:80%;
		border-radius:0;
		transform: rotate(-180deg);
	}
}

@keyframes ballbounce {
	/* up */
	0% {
		top:-30%;
		animation-timing-function: ease-in;
	}
	/* floor */
	30% {
		top:80%;
		animation-timing-function: ease-out;
	}
	/* up */
	40% {
		top: 20%;
	}
	/* up */
	45% {
		top:17%;
		animation-timing-function: ease-in;
	}
	/* floor */
	60% {
		top:80%;
		animation-timing-function: ease-out;
	}
	/* up */
	75% {
		top:30%;
	}
	90% {
		top:25%;
		animation-timing-function: ease-in;
	}
	/* floor */
	100% {
		top:110%;
		animation-timing-function:ease-out;
	}
}

@keyframes scalemask {
	0% {
		mask-size:0%;
	}
	65% {
		mask-size:0%;
	}
	78%,100% {
		mask-size:300%;
	}
}

@keyframes scalemask2 {
	0% {
		-webkit-mask-size:0%;
	}
	83% {
		-webkit-mask-size:0%;
	}
	100% {
		-webkit-mask-size: 300%;
	}
}

* {
	box-sizing:border-box;
}

body {
	padding:0;
	margin: 0;
}

/* Ball -------------------- */
.ball {
	width:5rem;
	height:5rem;
	left:50%;
	position:absolute;
	z-index:1;
	margin-left:-2.5rem;
	animation:ballbounce 4s 1s infinite;
	animation-fill-mode:both;
}

.ball:after {
	content:" ";
	color:#fff;
	display:block;
	margin:auto;
	border-radius:50%;
	background:#fff;
	width:100%;
	height:100%;
	animation: balltransform 4s 1s infinite;
}

/* Animation containers -------------------- */
.animation {
	background:#297acb;
	height:100vh;
	width:100vw;
	position:relative;
	z-index:1;
}

.animation-2,
.animation-3 {
	position:absolute;
	top:0;
	left:0;
	-webkit-mask-size:0;
	-webkit-mask-image:radial-gradient(circle closest-side,black 0%,black 90%,rgba(255,255,255,0) 92%);
	-webkit-mask-repeat:no-repeat;
	-webkit-mask-position:center center;
	animation-fill-mode:both;
}

.animation-2 {
	background:purple;
	animation:scalemask 4s 1s infinite;
}

.animation-3 {
	animation:scalemask2 4s 1s infinite;
}

.animation-2 .ball:after {
	background: #297acb;
}
````

### Reading

Read the following articles and/or review the following examples on CSS animations:

* [Read this article on CSS Transforms](http://learn.shayhowe.com/advanced-html-css/css-transforms/)
* [Read this article on CSS Transitions &amp; Animations](http://learn.shayhowe.com/advanced-html-css/transitions-animations/)
* [8 simple CSS3 transitions that will wow your users](http://www.webdesignerdepot.com/2014/05/8-simple-css3-transitions-that-will-wow-your-users)
* [6 Buttons animated](http://codepen.io/retyui/pen/ByoaXV)
* [CSS3 Animations: Keyframes](http://codepen.io/akshaychauhan/pen/oAfae)
* [404](http://codepen.io/kieranfivestars/pen/MYdQxX)
* [Pure CSS Bounce Animation](http://codepen.io/dp_lewis/pen/gCfBv)

[<== Previous Lesson](class-13.md) [Next Lesson ==>](class-15.md)

[<== Home](README.md) 🏠
