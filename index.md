<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta http-equiv="X-UA-Compatible" content="IE=edge">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>电子通行证</title>
  <style>
    html, body {
      width: 100%;
      height: 100%;
      margin: 0;
      padding: 0;
    }
    .box {
      width: 100%;
      height: 100%;
      background: url('./wepback.jpeg');
      background-size: 100%;
      background-repeat: no-repeat;
    }
    #date {
      font-size: 32px;
      position: absolute;
      text-align: center;
      top: 200px;
      width: 100%;
    }
    #time {
      font-size: 32px;
      position: absolute;
      text-align: center;
      top: 248px;
      width: 100%;
    }
  </style>
</head>
<body>
  <div class="box">
    <div id="date"></div>
    <div id="time"></div>
  </div>
</body>
<script>
  window.onload = function () {
    var date = document.getElementById('date');
    var time = document.getElementById('time');
    setInterval(() => {
      var now = new Date();
      var month = now.getMonth() + 1;
      var day = now.getDate();
      var hour = now.getHours();
      var minute = now.getMinutes();
      var second = now.getSeconds();
      if (hour < 10) {
        hour = '0' + hour;
      }
      if (minute < 10) {
        minute = '0' + minute;
      }
      if (second < 10) {
        second = '0' + second;
      }
      date.innerHTML = month + '月' + day + '日';
      time.innerHTML = hour + ':' + minute + ':' + second;
    }, 1000)
  }
</script>
</html>
