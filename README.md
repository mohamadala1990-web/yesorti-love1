<!DOCTYPE html>
<html lang="ar">
<head>
<meta charset="UTF-8">
<title>هل تحبيني ❤️</title>

<style>
body{
    margin:0;
    height:100vh;
    display:flex;
    justify-content:center;
    align-items:center;
    background:linear-gradient(135deg,#ff9ecf,#ff69b4);
    overflow:hidden;
    font-family:Tahoma;
}

.box{
    text-align:center;
    background:rgba(255,255,255,.25);
    padding:30px;
    border-radius:25px;
}

h1{
    color:white;
    font-size:38px;
}

button{
    border:0;
    padding:15px 35px;
    margin:15px;
    border-radius:15px;
    font-size:22px;
    cursor:pointer;
}

#yes{
    background:#ff1493;
    color:white;
}

#no{
    background:white;
    position:absolute;
}

#msg{
    display:none;
    color:white;
    font-size:30px;
    margin-top:20px;
}

.heart{
    position:absolute;
    color:white;
    font-size:25px;
    animation:up 5s linear infinite;
}

@keyframes up{
    from{
        transform:translateY(100vh);
    }
    to{
        transform:translateY(-100px);
    }
}
</style>

</head>

<body>

<div class="box">

<h1>هل تحبيني؟ ❤️</h1>

<button id="yes" onclick="yesClick()">نعم ❤️</button>
<button id="no">لا 😭</button>

<div id="msg"></div>

</div>


<script>

let no = document.getElementById("no");
let yes = document.getElementById("yes");

let size = 22;

function escapeNo(){

    let x = Math.random() * (window.innerWidth - 100);
    let y = Math.random() * (window.innerHeight - 50);

    no.style.left = x + "px";
    no.style.top = y + "px";

    size += 5;

    yes.style.fontSize = size + "px";
}


no.addEventListener("mouseover", escapeNo);
no.addEventListener("touchstart", escapeNo);


function yesClick(){

document.getElementById("msg").style.display="block";
document.getElementById("msg").innerHTML =
"عرفت إنك تحبيني 🥹❤️";

}


// قلوب تطير
setInterval(function(){

let h=document.createElement("div");

h.className="heart";
h.innerHTML="❤️";
h.style.left=Math.random()*100+"%";
h.style.animationDuration=(3+Math.random()*3)+"s";

document.body.appendChild(h);

setTimeout(()=>h.remove(),6000);

},300);

</script>

</body>
</html>
