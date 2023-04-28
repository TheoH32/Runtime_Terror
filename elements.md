---
title: Binary Guessing Game
layout: page
description: "Try it out!"
image: assets/images/translate.jpg
nav-menu: true
---


<style>
    *{
        background-color:darkcyan;
        
    }

    #answerBox {
        font-size:large;
        padding: 0%;
        word-spacing: 1px;
    }
    .label {
        font-size: 500px;
    }
    .vl {
        border-left: 6px solid green;
        height: 300px;
        position: absolute;
        left: 0.2%;
        margin-left: -3px;
        top: 0;
        font-size: 600px;
    }
    .vl2 {
        border-left: 6px solid green;
        height: 300px;
        position: absolute;
        left: 12.5%;
        margin-left: -3px;
        top: 0;
      }
    .vl3 {
        border-left: 6px solid green;
        height: 300px;
        position: absolute;
        left: 24.9%;
        margin-left: -3px;
        top: 0;
      }
    .vl4 {
        border-left: 6px solid green;
        height: 300px;
        position: absolute;
        left: 37.3%;
        margin-left: -3px;
        top: 0;
      }
    .vl5 {
        border-left: 6px solid green;
        height: 300px;
        position: absolute;
        left: 87%;
        margin-left: -3px;
        top: 0;
        padding:0%;
      }
      
    .vl6 {
        border-left: 6px solid green;
        height: 300px;
        position: absolute;
        left: 49.7%;
        margin-left: -3px;
        top: 0;
        }
    .vl7 {
        border-left: 6px solid green;
        height: 300px;
        position: absolute;
        left: 62.1%;
        margin-left: -3px;
        top: 0;
        }
    .vl8 {
        border-left: 6px solid green;
        height: 300px;
        position: absolute;
        left: 74.5%;
        margin-left: -3px;
        top: 0;
        opacity: 1;
        }
    .vl9 {
        border-left: 6px solid green;
        height: 300px;
        position: absolute;
        left: 99.9%;
        margin-left: -3px;
        top: 0;
        }

    .lower{
        position: relative;
        bottom: 1450px;
        align-items: center;
        text-align: center;
    }
    #ps1 {
		position: relative;
		left: 6%;
		top: 17px;
        font-size:60px;
	}
    #ps2 {
        position: relative;
        left: 18%;
		bottom: 200px;
        font-size:60px;

    }

    #ps3 {
        position: relative;
        left: 30.5%;
		bottom: 417px;
        font-size:60px;
    }

    #ps4 {
        position: relative;
        left: 43%;
        bottom: 636px;
        font-size:60px;
    }

    #ps5 {
        position: relative;
        left: 55%;
        bottom: 855px;
        font-size:60px;
    }

    #ps6 {
        position: relative;
        left: 67.3%;
		bottom: 1072px;
        font-size:60px;
    }

    #ps7 {
        position: relative;
        left: 79.5%;
        bottom: 1290px;
        font-size:60px;
        padding:0%;
    }

    #ps8 {
        position: relative;
        left: 92%;
        bottom: 1508px;
        font-size:60px;
    }
    
    #user-answer{
        color:black;
    }

    


</style>


<body class="flex">

<div class="space1">
    <div class="vl"></div>
    <div id="ps1"></div>

</div>

<div class="space2">
    <div class="vl2"></div>
    <div id="ps2"></div>
</div>

<div class="space3">
    <div class="vl3"></div>
    <div id="ps3"></div>
</div>

<div class="space4">
    <div class="vl4"></div>
    <div id="ps4"></div>
</div>

<div class="space5">
    <div class="vl5"></div>
    <div id="ps5"></div>
</div>

<div class="space6">
    <div class="vl6"></div>
    <div id="ps6"></div>
</div>

<div class="space7">
    <div class="vl7"></div>
    <div id="ps7"></div>
</div>

<div class="space8">
    <div class="vl8"></div>
    <div id="ps8"></div>
</div>
    <div class="vl9"></div>

<div class="lower">
    <div id="answerBox">
            <form id = "form1">
                <label for="user-answer">Answer:</label>
                <input type="number" id="user-answer" /><br />
                <input type="submit" id="submit-button"  value="Submit" />
            </form>
    </div>
    <div id="score">
        <h3>
            Score: <span id = "scoreVal"></span>
        </h3>
    </div>

</div>

<script>

    const _ps1 = document.getElementById("ps1")
    const _ps2 = document.getElementById("ps2")
    const _ps3 = document.getElementById("ps3")
    const _ps4 = document.getElementById("ps4")
    const _ps5 = document.getElementById("ps5")
    const _ps6 = document.getElementById("ps6")
    const _ps7 = document.getElementById("ps7")
    const _ps8 = document.getElementById("ps8")
    const _verify = document.getElementById("submit-button")
    //const _answerInput = document.getElementById("user-answer")
    const _form = document.getElementById("form1") 
    const _score = document.getElementById('scoreVal');
    let score = 0


    function randNum1(){
        a = Math.round(Math.random());
    }
    function randNum2(){
        b = Math.round(Math.random());
    }
    function randNum3(){
        c = Math.round(Math.random());
    }
    function randNum4(){
        d = Math.round(Math.random());
    }
    function randNum5(){
        e = Math.round(Math.random());
    }
    function randNum6(){
        f = Math.round(Math.random());
    }
    function randNum7(){
        g = Math.round(Math.random());
    }
    function randNum8(){
        h = Math.round(Math.random());
    }


    function binArray(){
        randNum1();
        randNum2();
        randNum3();
        randNum4();
        randNum5();
        randNum6();
        randNum7();
        randNum8();
        const binaryArray = [`${a}`, `${b}`, `${c}`, `${d}`, `${e}`, `${f}`, `${g}`, `${h}`];
        console.log(binaryArray);
        binaryNum = binaryArray.join("");
        console.log(binaryNum);
		const parseArray = binaryArray => {
			const binaryString = binaryArray.join("");
			return parseInt(binaryString, 2);
		 };

	    var x = parseArray(binaryArray);
		console.log(x);

        // for (let i = 0; i < binaryArray.length; i++) {
        //     if(binaryArray[i] = 0) {
        //         console.log("yes");
        //     }
        // }
        binaryArray.forEach((item) => {
            if(item == 1){
                console.log("yes");
                
            }
            console.log(item);

        });


        checkAns(x);
        

    function checkAns(i){
        
    _verify.addEventListener('click', (event) => {
        event.preventDefault(); // prevent form submission
        // get the form data

        let answer = document.getElementById("user-answer").value;
        const formData = new FormData(_form);
        const name = formData.get(answer);
        // do something with the form data
        if (answer == i && answer !== ""){
            console.log("Wow, you are so smart!");
            score = score + 1;
            formData.get(answer)
            } else if (answer !== "" && answer !== i)  {
                console.log("You are a disgrace to your family!")
//                life = life - 1;
  //              console.log(life);
    //            if(life == 0){
      //              location.reload();
        //        }

            }
        printNum();
    });
    
    }


//        checkAns(_answer, x)
}


//    function checkAns(a, b){
  //      if(a == b){
    //        console.log("WINNNN")
//        }
  //  }
    
    function printNum(){
        binArray();
        _ps1.innerHTML = `<p> ${a} <p>`
        _ps2.innerHTML = `<p> ${b} <p>`
        _ps3.innerHTML = `<p> ${c} <p>`
        _ps4.innerHTML = `<p> ${d} <p>`
        _ps5.innerHTML = `<p> ${e} <p>`
        _ps6.innerHTML = `<p> ${f} <p>`
        _ps7.innerHTML = `<p> ${g} <p>`
        _ps8.innerHTML = `<p> ${h} <p>`
        _score.innerHTML = `${score}`
        
    }

printNum();


</script>
