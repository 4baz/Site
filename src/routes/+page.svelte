
<script>
// @ts-nocheck
const MusicURL = new URL('../../static/favicon.png', import.meta.url).href
console.log(MusicURL);
    import IndexNested from "./IndexNested.svelte";
	import { onMount } from 'svelte';
    var textarray = [
        "I make things, they're not very good",
        "microplastic enjoyer",
        "Ethereal Hater",
        "bad coder",
        ".net is for retards",
        "I hate frontend web development, it sucks",
        "Reversal god",
        "Slags Only coming 2023",
        "kekw",
        "Owner of shitpissandcum.xyz",
        "Owner of Cybercrime.pw",
        "UwU",
        "Skid",
        "yo",
        ":)",
        "VicSocialists Supporter",
        "Uses Cracked IDA",
        "Ghidra is Spyware",
        "Cheat Engine Enthusiant",
        "Monarch Upload Fanboy",
        "lulw"];


        // @ts-ignore
        Array.prototype.random = function () {
            return this[Math.floor((Math.random()*this.length))];
          }


        function swaptext(){

       // @ts-ignore
       return textarray.random();

        }
    let switchedtext = swaptext();

    let c;

    //funni js shit for matrix

    onMount(() => {
      const ctx = c.getContext('2d');
//making the canvas full screen
c.height = window.innerHeight;
c.width = window.innerWidth;

//chinese characters - taken from the unicode charset
var matrix = "abcdefghijklmnopqrstuvwxyzABCDEFGHIJKLMNOPQRSTUVWXYZ123456789@#$%^&*()*&^%+-/~{[|`]}";
//converting the string into an array of single characters
matrix = matrix.split("");

var font_size = 10;
var columns = c.width/font_size; //number of columns for the rain
//an array of drops - one per column
var drops = [];
//x below is the x coordinate
//1 = y co-ordinate of the drop(same for every drop initially)
for(var x = 0; x < columns; x++)
    drops[x] = 1;

//drawing the characters
function draw()
{
    //Black BG for the canvas
    //translucent BG to show trail
    ctx.fillStyle = "rgba(0, 0, 0, 0.04)";
    ctx.fillRect(0, 0, c.width, c.height);

    ctx.fillStyle = "#CC00CC";// text colour
    ctx.font = font_size + "px arial";
    //looping over drops
    for(var i = 0; i < drops.length; i++)
    {
        //a random chinese character to print
        var text = matrix[Math.floor(Math.random()*matrix.length)];
        //x = i*font_size, y = value of drops[i]*font_size
        ctx.fillText(text, i*font_size, drops[i]*font_size);

        //sending the drop back to the top randomly after it has crossed the screen
        //adding a randomness to the reset to make the drops scattered on the Y axis
        if(drops[i]*font_size > c.height && Math.random() > 0.975)
            drops[i] = 0;

        //incrementing Y coordinate
        drops[i]++;
    }
}

setInterval(draw, 35);

    });

</script>
<style>
canvas{
          position:absolute;
          left:0;
          top:0;
          z-index:-1;

      }
</style>
<canvas bind:this={c}>

</canvas>
<div class="">


<div class="container object-none object-center mx-auto  px-7  text-white">

    <!--<h1>Yo</h1><br>
    <p>Python,c++,c,js</p>-->

    <IndexNested/>

<!-- use the nested css thing here to create homepage css maybe based of

    og site but maybe text background from oasis
-->

<h1 class=" text-center text-xl">{switchedtext}</h1>



</div>
</div>
