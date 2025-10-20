# Sabo-quiz
<!doctype html>

<html lang="pl">
<head>
  <meta charset="utf-8">
  <meta name="viewport" content="width=device-width,initial-scale=1">
  <title>Quiz: Sabotażysta — Sezon 4</title>
  <style>
    body{font-family:Inter,system-ui,Segoe UI,Roboto,'Helvetica Neue',Arial;margin:0;background:#0f172a;color:#e6eef8;padding:2rem}
    .card{background:#0b1220;border-radius:12px;padding:20px;max-width:900px;margin:0 auto;box-shadow:0 6px 30px rgba(2,6,23,.6)}
    h1{font-size:1.6rem;margin:0 0 10px}
    p.lead{opacity:.9}
    .q{margin:16px 0;padding:12px;border-radius:8px;background:rgba(255,255,255,.02)}
    label{display:block;margin:6px 0;cursor:pointer}
    button{background:#1f2937;color:#fff;border:0;padding:10px 14px;border-radius:8px;font-weight:600;cursor:pointer}
    .result{margin-top:16px;padding:12px;border-radius:8px;background:rgba(255,255,255,.03)}
    footer{margin-top:18px;opacity:.7;font-size:.85rem}
    .correct{color:limegreen;font-weight:700}
    .wrong{color:#ff6b6b;font-weight:700}
  </style>
</head>
<body>
  <div class="card">
    <h1>Quiz: Sabotażysta — Sezon 4</h1>
    <p class="lead">10 pytań sprawdzających wiedzę o 4. sezonie. Po zakończeniu kliknij "Sprawdź odpowiedzi".</p><form id="quiz">

  <div class="q">
    <strong>Pytanie 1.</strong> Kiedy miał premierę 4. sezon "Sabotażysty"? <br>
    <label><input type="radio" name="q1" value="A"> A) 2 października 2025</label>
    <label><input type="radio" name="q1" value="B"> B) 1 września 2025</label>
    <label><input type="radio" name="q1" value="C"> C) 3 października 2024</label>
  </div>

  <div class="q">
    <strong>Pytanie 2.</strong> Gdzie kręcono 4. sezon (miejsce akcji)?<br>
    <label><input type="radio" name="q2" value="A"> A) Kołobrzeg</label>
    <label><input type="radio" name="q2" value="B"> B) Zakopane</label>
    <label><input type="radio" name="q2" value="C"> C) Mazury</label>
  </div>

  <div class="q">
    <strong>Pytanie 3.</strong> Który z poniższych uczestników NIE był wymieniony w medialnych zapowiedziach jako biorący udział w S4?<br>
    <label><input type="radio" name="q3" value="A"> A) Tymoteusz Puchacz</label>
    <label><input type="radio" name="q3" value="B"> B) Sebastian Fabijański</label>
    <label><input type="radio" name="q3" value="C"> C) Robert Lewandowski</label>
  </div>

  <div class="q">
    <strong>Pytanie 4.</strong> Ile osób brano na start do gry w 4. sezonie (zgodnie z doniesieniami)?<br>
    <label><input type="radio" name="q4" value="A"> A) 8</label>
    <label><input type="radio" name="q4" value="B"> B) 12</label>
    <label><input type="radio" name="q4" value="C"> C) 16</label>
  </div>

  <div class="q">
    <strong>Pytanie 5.</strong> Kto z poniższych był wymieniony jako uczestnik i jest aktorem?<br>
    <label><input type="radio" name="q5" value="A"> A) Patryk "Kizo" Woziński</label>
    <label><input type="radio" name="q5" value="B"> B) Sebastian Fabijański</label>
    <label><input type="radio" name="q5" value="C"> C) Tymoteusz Puchacz</label>
  </div>

  <div class="q">
    <strong>Pytanie 6.</strong> Które medium oficjalnie informowało o ofercie uczestników i dacie premiery S4? <br>
    <label><input type="radio" name="q6" value="A"> A) RMF.fm</label>
    <label><input type="radio" name="q6" value="B"> B) BBC News</label>
    <label><input type="radio" name="q6" value="C"> C) Al Jazeera</label>
  </div>

  <div class="q">
    <strong>Pytanie 7.</strong> Jak nazywa się twórca / producent programu podanym w mediach? <br>
    <label><input type="radio" name="q7" value="A"> A) Remigiusz Wierzgoń (Rezi)</label>
    <label><input type="radio" name="q7" value="B"> B) Robert Makłowicz</label>
    <label><input type="radio" name="q7" value="C"> C) Magda Gessler</label>
  </div>

  <div class="q">
    <strong>Pytanie 8.</strong> Czy w medialnych relacjach pojawiała się informacja o tym, że pierwszy odcinek trafił na listę trendów na YouTube? <br>
    <label><input type="radio" name="q8" value="A"> A) Tak</label>
    <label><input type="radio" name="q8" value="B"> B) Nie</label>
  </div>

  <div class="q">
    <strong>Pytanie 9.</strong> Które z poniższych nazwisk pojawia się w relacjach jako uczestniczka i influencerka zwyciężczyni innego programu? <br>
    <label><input type="radio" name="q9" value="A"> A) Natalia "Natsu" Karczmarczyk</label>
    <label><input type="radio" name="q9" value="B"> B) Marta Kaczyńska</label>
    <label><input type="radio" name="q9" value="C"> C) Anna Lewandowska</label>
  </div>

  <div class="q">
    <strong>Pytanie 10.</strong> Czy sezony "Sabotażysty" publikowane są głównie na kanale Reziego (YouTube)? <br>
    <label><input type="radio" name="q10" value="A"> A) Tak</label>
    <label><input type="radio" name="q10" value="B"> B) Nie</label>
  </div>

  <button type="button" id="check">Sprawdź odpowiedzi</button>
</form>

<div class="result" id="result" aria-live="polite" hidden></div>

<footer>Stworzono automatycznie: quiz ma charakter nieoficjalny i opiera się na doniesieniach medialnych.</footer>

  </div>  <script>
    const answers = {q1:'A', q2:'A', q3:'C', q4:'B', q5:'B', q6:'A', q7:'A', q8:'A', q9:'A', q10:'A'};
    document.getElementById('check').addEventListener('click', ()=>{
      const form = document.forms['quiz'];
      let score=0; let total=Object.keys(answers).length; let detail = [];
      for(let i=1;i<=total;i++){
        const name='q'+i; const val = form[name].value;
        const ok = answers[name];
        if(val===ok){score++; detail.push(`<div>${i}. <span class="correct">OK</span></div>`)}
        else if(!val){detail.push(`<div>${i}. <span class="wrong">Brak odpowiedzi (poprawna: ${ok})</span></div>`)}
        else{detail.push(`<div>${i}. <span class="wrong">Źle (twoje: ${val}; poprawna: ${ok})</span></div>`) }
      }
      const res = document.getElementById('result');
      res.hidden=false; res.innerHTML = `<strong>Wynik: ${score}/${total}</strong><div style="margin-top:8px">${detail.join('')}</div>`;
    });
  </script></body>
</html>
