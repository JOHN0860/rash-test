<!DOCTYPE html>
<html lang="uz">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Test yechish</title>

<link rel="stylesheet" href="https://unpkg.com/mathlive/dist/mathlive.core.css">
<link rel="stylesheet" href="https://unpkg.com/mathlive/dist/mathlive.css">
<script src="https://unpkg.com/mathlive"></script>

<style>
body{font-family:Arial;background:#f4f6f8;padding:10px}
.card{background:#fff;border-radius:12px;padding:12px;margin-bottom:12px}
.variant{padding:10px 14px;border-radius:10px;background:#e0e0e0;cursor:pointer}
.variant.active{background:#1976d2;color:#fff}
.variants{display:flex;gap:8px;flex-wrap:wrap}
.mathbox{width:100%;min-height:50px;font-size:22px;border:2px solid #ccc;border-radius:10px;padding:8px}
button{width:100%;padding:14px;font-size:18px;border:none;border-radius:12px;background:#1976d2;color:#fff}
input{width:100%;padding:12px;font-size:18px;border-radius:10px;border:2px solid #ccc}
</style>
</head>

<body>

<div class="card">
  <h3>Test kodi</h3>
  <input id="testCode" placeholder="Masalan: MT-834921">
  <button onclick="loadTest()">Testni ochish</button>
</div>

<div id="testArea"></div>

<script>
let testData = null;
let answers = {};

function loadTest(){
  const code = document.getElementById("testCode").value.trim();
  const saved = localStorage.getItem("TEST_"+code);
  if(!saved){
    alert("❌ Noto‘g‘ri test kodi");
    return;
  }
  testData = JSON.parse(saved);
  renderTest();
}

function renderTest(){
  const area = document.getElementById("testArea");
  area.innerHTML = "";

  testData.questions.forEach(q=>{
    let html = `<div class="card"><b>${q.id}-savol</b>`;

    if(q.type==="variant"){
      html+=`<div class="variants">`;
      q.options.forEach(o=>{
        html+=`<div class="variant" onclick="pick(${q.id},'${o}',this)">${o}</div>`;
      });
      html+=`</div>`;
    }

    if(q.type==="math"){
      html+=`
        <div>(a)</div>
        <math-field class="mathbox"
          virtual-keyboard-mode="onfocus"
          oninput="answers[${q.id+'_a'}]=this.value"></math-field>
        <div>(b)</div>
        <math-field class="mathbox"
          virtual-keyboard-mode="onfocus"
          oninput="answers[${q.id+'_b'}]=this.value"></math-field>`;
    }

    html+=`</div>`;
    area.innerHTML+=html;
  });

  area.innerHTML+=`<button onclick="finish()">Yuborish</button>`;
}

function pick(id,val,el){
  el.parentElement.querySelectorAll(".variant").forEach(v=>v.classList.remove("active"));
  el.classList.add("active");
  answers[id]=val;
}

function finish(){
  let correct=0;
  testData.questions.forEach(q=>{
    if(q.type==="variant" && answers[q.id]===q.correct) correct++;
    if(q.type==="math"){
      if(answers[q.id+'_a']===q.correct.a) correct++;
      if(answers[q.id+'_b']===q.correct.b) correct++;
    }
  });

  const total=testData.total;
  const score=(correct/total)*75;
  let grade="Fail";
  if(score>=70) grade="A+";
  else if(score>=60) grade="A";
  else if(score>=50) grade="B";
  else if(score>=46) grade="C";

  alert(`✅ Natija:
To‘g‘ri: ${correct}
Noto‘g‘ri: ${total-correct}
Ball: ${score.toFixed(1)}
Daraja: ${grade}`);
}
</script>

</body>
</html>
