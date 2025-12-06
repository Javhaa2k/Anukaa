<html lang="mn">
<head>
  <meta charset="utf-8">
  <meta name="viewport" content="width=device-width,initial-scale=1">
  <title>Анука-д боломж</title>
  <style>
    :root{--bg:#f7f4fb;--card:#fff;--accent:#ff6b81;--muted:#666}
    *{box-sizing:border-box;font-family:Inter, "Noto Sans Mongolian", system-ui, -apple-system, "Segoe UI", Roboto, "Helvetica Neue", Arial}
    html,body{height:100%;margin:0;background:linear-gradient(135deg,#fef3f7 0%, #f0f7ff 100%)}
    .wrap{min-height:100%;display:flex;align-items:center;justify-content:center;padding:32px}

    .card{background:var(--card);padding:28px;border-radius:16px;box-shadow:0 10px 30px rgba(20,20,50,0.08);max-width:720px;width:100%;text-align:center}
    h1{margin:0 0 18px;font-size:26px;color:#222}
    p{color:var(--muted);line-height:1.5}

    .btn-row{display:flex;gap:12px;justify-content:center;margin-top:20px}
    button{padding:12px 20px;border-radius:10px;border:0;font-size:16px;cursor:pointer;box-shadow:0 6px 16px rgba(20,20,50,0.06)}
    .yes{background:var(--accent);color:white}
    .no{background:#eef2ff;color:#2b2b66}

    .hidden{display:none}

    .message{font-size:20px}

    /* small responsive tweak */
    @media (max-width:420px){.card{padding:20px}h1{font-size:20px}}
  </style>
</head>
<body>
  <div class="wrap">
    <div class="card" id="start">
      <h1>Анука жавхаад боломж олгох уу?</h1>
      <div class="btn-row">
        <button class="yes" id="yesBtn">Тийм</button>
        <button class="no" id="noBtn">Үгүй</button>
      </div>
    </div>

    <div class="card hidden" id="yesCard">
      <h1>Баярлалаа Анука</h1>
      <p class="message">Худлаа хэлсэнг минь уучлаарай. Чамайг алдахвы гэж айсандаа юм шүү. Дахиж чиний итгэлийг алдахгүй ээ. Хайртай шүү хөөрхнөө 💖</p>
    </div>

    <div class="card hidden" id="noCard">
      <h1>Алдаа гарсан байна😁</h1>
      </div>
  </div>

  <script>
    const yesBtn = document.getElementById('yesBtn');
    const noBtn = document.getElementById('noBtn');
    const start = document.getElementById('start');
    const yesCard = document.getElementById('yesCard');
    const noCard = document.getElementById('noCard');

    function show(el){ start.classList.add('hidden'); yesCard.classList.add('hidden'); noCard.classList.add('hidden'); el.classList.remove('hidden'); window.scrollTo({top:0,behavior:'smooth'}); }

    yesBtn.addEventListener('click',()=>{
      show(yesCard);
    });

    noBtn.addEventListener('click',()=>{
      show(noCard);
    });
  </script>
</body>
</html>
