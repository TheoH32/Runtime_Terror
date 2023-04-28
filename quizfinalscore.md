---
title: Quiz Score
layout: page
description: "Scoring"
image: assets/images/pic07.jpg
nav-menu: true
---

<script>
    displayScore = localStorage.getItem("finalScore");
    console.log(displayScore)
</script>

<style>
    .boxed {
        width:800px;
        margin: 30px auto;
        border: 5px solid grey;
    }

    h1 {
        margin: 20px;
        text-align: center;
    }

    h2 {
        text-align: center;
        color: blue;
    }

</style>

<div class="boxed">
    <h1>
    Score: <script type="text/javascript">document.write(displayScore)</script>/6
    </h1>
    <h2><a href="/Runtime-Terror/quiz.html">Try Again</a></h2>
</div>


