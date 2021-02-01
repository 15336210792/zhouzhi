# zhouzhi
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
<body>
    <script>
        // 获取随机数
        num= Math.floor(Math.random() * (100) + 1);
        function fn(){
            alert("准备好了吗？1~100以内的猜数字游戏要开始了哦!");
            alert("您有10次机会猜测哦，请把握机会哦！");
            for(var i=1;i<=10;i++){
                var guess=prompt("1~100以内的数字，请输入你猜测的数字！");
                if(guess==""){
                    alert("您还没有输入的任何数字哦！请输入数字吧！");
                }else if(isNaN(guess)){
                    alert("您输入的不是数字哦！请输入数字吧！");
                }else if(guess>100){
                    alert("第"+i+"次输入，您输入的数字太大了，大于我们的边界了！");
                }else if(guess<1){
                    alert("第"+i+"次输入，您输入的数字太小了，大于我们的边界了！");
                }else if(guess>num){
                    alert("这是您的第"+i+"次输入，这个数字太大了哦！换小一点吧！");
                    if(i==10){
                        alert(i+"次机会，您已经用完了，真遗憾！这个数字是"+num);
                        continue;
                    }
                }else if(guess<num){
                    alert("这是您的第"+i+"次输入，这个数字太小了哦！换大一点吧！");
                    if(i==10){
                        alert(i+"次机会，您已经用完了，真遗憾！这个数字是"+num);
                        continue;
                    }
                }else if(guess==num){
                    alert("您太棒了，答对了哦！恭喜你！");
                    continue;
                }
            }
        }

        fn();
    </script>
</body>
</html>
