
<script>
    import IndexNested from "./IndexNested.svelte";

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
        "Greens Supporter",
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
</script>

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
