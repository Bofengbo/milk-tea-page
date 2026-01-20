<!DOCTYPE html>
<html>
<head>
    <title>请我喝新年第一杯奶茶</title>
    <meta charset="utf-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, user-scalable=no">
    <!-- 新增微信适配meta标签 -->
    <meta name="wechat-webview-api-version" content="1.0">
    <style>
        body {
            background-color: #ffd1dc;
            text-align: center;
            padding-top: 80px;
            margin: 0;
            font-family: "Microsoft Yahei", "PingFang SC", "微软雅黑", sans-serif;
            overflow: hidden;
            /* 新增：防止微信长按选中文字 */
            -webkit-user-select: none;
            user-select: none;
        }
        .avatar {
            width: 200px;
            height: 200px;
            border-radius: 10px;
            margin-bottom: 30px;
            max-width: 80vw;
            max-height: 80vw;
        }
        h2 {
            color: #e91e63;
            margin-bottom: 40px;
            position: relative;
            z-index: 10;
            font-size: clamp(20px, 5vw, 28px);
        }
        .btn-container {
            position: relative;
            display: inline-block;
            z-index: 20;
        }
        .btn {
            padding: 15px 50px;
            margin: 20px;
            border-radius: 30px;
            border: none;
            font-size: 20px;
            cursor: pointer;
            font-weight: bold;
            transition: all 0.3s cubic-bezier(0.34, 1.56, 0.64, 1);
            position: relative;
            min-width: clamp(120px, 25vw, 160px);
            box-sizing: border-box;
            padding: clamp(10px, 3vw, 15px) clamp(30px, 8vw, 50px);
            /* 新增：微信里点击按钮的反馈 */
            -webkit-tap-highlight-color: transparent;
        }
        .btn-yes {
            background-color: #e91e63;
            color: white;
            transform-origin: center center;
            z-index: 21;
            box-shadow: 0 4px 12px rgba(233, 30, 99, 0.3);
        }
        .btn-yes:hover {
            background-color: #d81b60;
        }
        .btn-no {
            background-color: white;
            color: #e91e63;
            border: 2px solid #e91e63;
            z-index: 21;
            margin-left: 40px;
            transform-origin: center center;
            box-shadow: 0 4px 12px rgba(233, 30, 99, 0.1);
        }
        .thanks-box {
            display: none;
            position: fixed;
            top: 0;
            left: 0;
            width: 100vw;
            height: 100vh;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            background-color: #ffd1dc;
            z-index: 9999;
            opacity: 0;
            transform: translateY(20px);
            transition: all 0.5s ease;
        }
        .thanks-box.show {
            opacity: 1;
            transform: translateY(0);
        }
        .thanks-img {
            width: 200px;
            height: 200px;
            border-radius: 10px;
            margin-bottom: 40px;
            max-width: 50vw;
            max-height: 50vw;
        }
        .thanks-text {
            color: #e91e63;
            font-size: clamp(40px, 15vw, 100px);
            font-weight: bold;
            text-align: center;
            letter-spacing: 2px;
            padding: 0 20px;
            margin: 0;
        }
    </style>
</head>
<body>
    <img src="https://p11-flow-imagex-download-sign.byteimg.com/tos-cn-i-a9rns2rl98/9d56ec27c7db4c6da10065fffc5e4040.jpg~tplv-a9rns2rl98-24:720:720.image?lk3s=8e244e95&rcl=20260120120429954CC8D6F441725121B7&rrcfp=8a172a1a&x-expires=1769486669&x-signature=Ju1Itv7YBWqKysXprFLWdEPCVig%3D" class="avatar" alt="趣味咖啡图">
    <h2>可以请我喝新年的第一杯奶茶吗？</h2>
    <div class="btn-container">
        <button class="btn btn-yes" id="yesBtn">可以</button>
        <button class="btn btn-no" id="noBtn">不可以</button>
    </div>
    <div class="thanks-box" id="thanksBox">
        <img src="https://p26-flow-imagex-download-sign.byteimg.com/tos-cn-i-a9rns2rl98/cff0e2e8a1914a7dbfe37267529a6b15.png~tplv-a9rns2rl98-24:720:720.png?lk3s=8e244e95&rcl=20260120123432FF32C6F437D156547D27&rrcfp=8a172a1a&x-expires=1769488472&x-signature=iDsG1thGbYXZsceEPLmSGpytQ4M%3D" class="thanks-img" alt="感谢表情包">
        <p class="thanks-text">谢谢老板，老板大气🥤</p>
    </div>

    <script>
        document.addEventListener('DOMContentLoaded', function() {
            const yesBtn = document.getElementById('yesBtn');
            const noBtn = document.getElementById('noBtn');
            const thanksBox = document.getElementById('thanksBox');
            
            let yesScale = 1;
            const yesScaleStep = 0.5;
            const yesMaxScale = 4;
            
            let noScale = 1;
            const noScaleStep = 0.05;
            const noMinScale = 0.6;
            const avoidOverlapDistance = 150;

            function getSafePosition(targetX, targetY) {
                const viewportWidth = window.innerWidth;
                const viewportHeight = window.innerHeight;
                const btnMinWidth = noBtn.offsetWidth * noMinScale;
                const safeX = Math.max(btnMinWidth/2, Math.min(viewportWidth - btnMinWidth/2, targetX));
                const safeY = Math.max(btnMinWidth/2, Math.min(viewportHeight - btnMinWidth/2, targetY));
                return { x: safeX, y: safeY };
            }

            noBtn.addEventListener('click', function() {
                if (yesScale < yesMaxScale) {
                    yesScale += yesScaleStep;
                    yesBtn.style.transform = `scale(${yesScale})`;
                }

                const yesRect = yesBtn.getBoundingClientRect();
                const yesCenterX = yesRect.left + yesRect.width / 2;
                const yesCenterY = yesRect.top + yesRect.height / 2;

                const directionX = Math.random() > 0.5 ? 1 : -1;
                const directionY = Math.random() > 0.5 ? 1 : -1;
                const offsetX = directionX * (avoidOverlapDistance + Math.random() * 80);
                const offsetY = directionY * (avoidOverlapDistance + Math.random() * 80);
                const targetX = yesCenterX + offsetX;
                const targetY = yesCenterY + offsetY;
                const safePos = getSafePosition(targetX, targetY);

                noScale = Math.max(noMinScale, noScale - noScaleStep);

                const noRect = noBtn.getBoundingClientRect();
                const relX = safePos.x - noRect.left - noRect.width/2;
                const relY = safePos.y - noRect.top - noRect.height/2;
                noBtn.style.transform = `translate(${relX}px, ${relY}px) scale(${noScale})`;
            });

            yesBtn.addEventListener('click', function() {
                yesBtn.style.display = 'none';
                noBtn.style.display = 'none';
                document.querySelector('.avatar').style.display = 'none';
                document.querySelector('h2').style.display = 'none';
                thanksBox.style.display = 'flex';
                setTimeout(() => {
                    thanksBox.classList.add('show');
                }, 50);
            });

            window.addEventListener('resize', function() {
                if (noScale > noMinScale) {
                    noBtn.style.transform = 'translate(0, 0) scale(1)';
                    noScale = 1;
                    yesBtn.style.transform = 'scale(1)';
                    yesScale = 1;
                }
            });
        });
    </script>
</body>
</html>
