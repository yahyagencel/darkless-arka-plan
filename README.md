<!DOCTYPE html>
<html lang="tr">
<head>
<meta charset="UTF-8" />
<title>Yıldızlı Arka Plan</title>
<style>
  body, html {
    margin: 0; padding: 0; height: 100%;
    background: black;
    overflow: hidden;
  }
  .star {
    position: absolute;
    background: white;
    border-radius: 50%;
    opacity: 0.8;
    animation: twinkle 2s infinite alternate;
  }
  @keyframes twinkle {
    0% {opacity: 0.3;}
    100% {opacity: 1;}
  }
</style>
</head>
<body>
<script>
  const starCount = 100;
  for(let i=0; i<starCount; i++) {
    const star = document.createElement('div');
    star.classList.add('star');
    // Boyut
    const size = Math.random()*2 + 1; 
    star.style.width = size + 'px';
    star.style.height = size + 'px';
    // Konum
    star.style.top = Math.random()*window.innerHeight + 'px';
    star.style.left = Math.random()*window.innerWidth + 'px';
    // Animasyon gecikmesi
    star.style.animationDelay = (Math.random()*2) + 's';
    document.body.appendChild(star);
  }
</script>
</body>
</html>
