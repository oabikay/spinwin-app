<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Aledoy Academy - Lucky Spin Break</title>
    <!-- Bootstrap 5 CSS CDN -->
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/css/bootstrap.min.css" rel="stylesheet">
    
    <style>
        body {
            background-color: #f8f9fa; /* Clean off-white from site */
            color: #212529; 
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            min-height: 100vh;
            display: flex;
            align-items: center;
            justify-content: center;
            overflow-x: hidden; /* Prevent horizontal scrollbars */
        }

        .text-brand-red { color: #dc3545; }
        
        .btn-brand-dark {
            background-color: #000000;
            color: #ffffff;
            border-radius: 30px; /* Pill shape */
            transition: all 0.2s ease;
            font-size: 0.95rem;
            letter-spacing: 0.5px;
        }
        .btn-brand-dark:hover:not(:disabled) {
            background-color: #dc3545;
            color: #ffffff;
        }

        /* Responsive structural container for the wheel */
        .wheel-stage {
            position: relative;
            width: 100%;
            max-width: 360px;
            aspect-ratio: 1 / 1;
            margin: 0 auto;
        }

        /* Top Red Pointer Arrow */
        .pointer-arrow {
            position: absolute;
            top: -15px;
            left: 50%;
            transform: translateX(-50%);
            width: 0;
            height: 0;
            border-left: 16px solid transparent;
            border-right: 16px solid transparent;
            border-top: 28px solid #dc3545; 
            z-index: 10;
            filter: drop-shadow(0px 4px 5px rgba(0,0,0,0.15));
        }

        /* Dark frame holding the canvas */
        .outer-rim {
            width: 100%;
            height: 100%;
            border-radius: 50%;
            border: 12px solid #111111; 
            box-shadow: 0 12px 28px rgba(0,0,0,0.12);
            background-color: #111111;
            padding: 2px;
        }

        canvas {
            width: 100%;
            height: 100%;
            border-radius: 50%;
            display: block;
        }

        /* Center Cap Hub */
        .wheel-hub {
            position: absolute;
            width: 80px;
            height: 80px;
            background-color: #000000;
            border: 3px solid #ffffff;
            border-radius: 50%;
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%);
            z-index: 5;
            box-shadow: 0 4px 8px rgba(0,0,0,0.2);
            display: flex;
            align-items: center;
            justify-content: center;
            font-weight: bold;
            font-size: 0.75rem;
            color: #fff;
            letter-spacing: 0.5px;
        }
    </style>
</head>
<body>

<div class="container py-4">
    <div class="row justify-content-center">
        <div class="col-12 col-sm-10 col-md-6 col-lg-4">
            <!-- Main Card Container -->
            <div class="bg-white rounded-4 p-4 shadow-sm border border-light text-center">
                
                <!-- Brand Heading Layout -->
                <div class="mb-4">
                    <h4 class="mb-0 text-dark" style="font-weight: 800; letter-spacing: -0.5px;">
                        ALEDOY <span class="text-brand-red">ACADEMY</span>
                    </h4>
                    <div class="text-muted small mt-1">Break Time • Try Your Luck</div>
                </div>

                <!-- Wheel Elements Container -->
                <div class="py-2">
                    <div class="wheel-stage">
                        <div class="pointer-arrow"></div>
                        <div class="outer-rim">
                            <canvas id="wheelCanvas" width="500" height="500"></canvas>
                        </div>
                        <div class="wheel-hub">ALEDOY</div>
                    </div>
                </div>

                <!-- Spin Trigger Control -->
                <div class="mt-4 d-grid px-2">
                    <button id="spinBtn" class="btn btn-brand-dark btn-lg fw-bold text-uppercase py-2.5">Spin Wheel</button>
                </div>
                
                <!-- Dynamic Alert Box Output Area -->
                <div id="resultAlert" class="alert alert-light mt-4 fw-medium fs-6 shadow-sm py-3 mb-0" role="alert" style="min-height: 58px;">
                    Spin the wheel to win a break-time perk!
                </div>

            </div>
        </div>
    </div>
</div>

<script>
    const prizes = [
        { label: "📶 Free Data",      color: "#dc3545" },                       
        { label: "☕ Coffee Break",   color: "#2d3142" },                       
        { label: "Back to Code!",     color: "#f8f9fa", textColor: "#212529" }, 
        { label: "🍩 Snack Pack",     color: "#ffffff", textColor: "#212529" }, 
        { label: "🥤 Soft Drink",     color: "#dc3545" },                       
        { label: "🥪 Free Sub",       color: "#2d3142" },                       
        { label: "Back to Code!",     color: "#f8f9fa", textColor: "#212529" }, 
        { label: "⏰ 10m Early Out",  color: "#ffffff", textColor: "#212529" }  
    ];

    const canvas = document.getElementById("wheelCanvas");
    const ctx = canvas.getContext("2d");
    const spinBtn = document.getElementById("spinBtn");
    const resultAlert = document.getElementById("resultAlert");

    const totalSegments = prizes.length;
    const arcSize = (2 * Math.PI) / totalSegments;

    let currentAngle = 0;
    let isSpinning = false;

    function drawWheel() {
        ctx.clearRect(0, 0, canvas.width, canvas.height);
        const radius = canvas.width / 2;

        for (let i = 0; i < totalSegments; i++) {
            const angle = currentAngle + (i * arcSize);
            
            ctx.fillStyle = prizes[i].color;
            ctx.beginPath();
            ctx.moveTo(radius, radius);
            ctx.arc(radius, radius, radius, angle, angle + arcSize, false);
            ctx.lineTo(radius, radius);
            ctx.fill();

            ctx.strokeStyle = "rgba(0,0,0,0.05)";
            ctx.lineWidth = 2;
            ctx.stroke();

            ctx.save();
            ctx.fillStyle = prizes[i].textColor || "#ffffff";
            ctx.textBaseline = "middle";
            ctx.textAlign = "right";
            ctx.font = "bold 16px sans-serif";
            
            if(!prizes[i].textColor) {
                ctx.shadowColor = "rgba(0,0,0,0.3)";
                ctx.shadowBlur = 4;
            }

            ctx.translate(radius, radius);
            ctx.rotate(angle + (arcSize / 2));
            ctx.fillText(prizes[i].label, radius - 30, 0);
            ctx.restore();
        }
    }

    function spin() {
        if (isSpinning) return;

        isSpinning = true;
        spinBtn.disabled = true;
        resultAlert.className = "alert alert-light mt-4 fw-normal fs-6 shadow-sm py-3";
        resultAlert.innerHTML = `<div class="spinner-border spinner-border-sm text-danger me-2" role="status"></div>Selecting your fortune...`;

        const spinDuration = 4000; 
        const startTime = performance.now();
        
        const startAngle = currentAngle;
        const totalRotationToGo = (Math.PI * 2 * (5 + Math.floor(Math.random() * 4))) + (Math.random() * Math.PI * 2);

        function animateSpin(currentTime) {
            const elapsed = currentTime - startTime;
            const progress = Math.min(elapsed / spinDuration, 1);

            const easeOutCubic = 1 - Math.pow(1 - progress, 3);
            currentAngle = startAngle + (totalRotationToGo * easeOutCubic);

            drawWheel();

            if (progress < 1) {
                requestAnimationFrame(animateSpin);
            } else {
                isSpinning = false;
                spinBtn.disabled = false;
                calculateWinner();
            }
        }

        requestAnimationFrame(animateSpin);
    }

    function calculateWinner() {
        const normalizedAngle = (currentAngle % (Math.PI * 2) + (Math.PI * 2)) % (Math.PI * 2);
        const pointerCorrection = (1.5 * Math.PI);
        let winningIndex = Math.floor((pointerCorrection - normalizedAngle) / arcSize) % totalSegments;
        if (winningIndex < 0) winningIndex += totalSegments;

        const wonPrize = prizes[winningIndex];
        resultAlert.className = "alert mt-4 fw-bold fs-5 shadow-sm py-3";
        
        if (wonPrize.label.includes("Back to Code!")) {
            resultAlert.classList.add("alert-danger");
            resultAlert.innerHTML = "💻 Empty Slot! Back to work, code awaits you!";
        } else {
            resultAlert.classList.add("alert-success");
            resultAlert.innerHTML = `🎉 You won: <strong>${wonPrize.label}</strong>! Enjoy!`;
        }
    }

    spinBtn.addEventListener("click", spin);
    drawWheel();
</script>

</body>
</html>