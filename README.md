
<!DOCTYPE html>
<html>
<head>
    <title>Animation</title>
</head>
<body>
<canvas id="myCanvas" width="400" height="300" style="border:1px solid #000000;"></canvas>
<script>
    const canvas = document.getElementById('myCanvas');
    const ctx = canvas.getContext('2d');

    let x = 50, dx = 5;

    function animate() {
        ctx.clearRect(0, 0, canvas.width, canvas.height);

        // رسم دایره
        ctx.beginPath();
        ctx.arc(x, 150, 30, 0, Math.PI * 2);
        ctx.fillStyle = 'red';
        ctx.fill();

        // به‌روزرسانی موقعیت
        x += dx;
        if (x > 350 || x < 50) {
            dx = -dx;
        }

        requestAnimationFrame(animate);
    }

    animate();
</script>
</body>
</html>
