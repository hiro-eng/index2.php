
<!DOCTYPE html>
<html lang="en">
<head>
    <title>Document</title>
</head>
<body>
    

<h1>いま何時？</h1>

<p>いま
<?php
  date_default_timezone_set('Asia/Tokyo');
  echo date("Y 年 m 月 d 日 H 時 i 分 s 秒");
?>
です。</p>


<p>今日は
<?php
  $week[0] = "日";
  $week[1] = "月";
  $week[2] = "火";
  $week[3] = "水";
  $week[4] = "木";
  $week[5] = "金";
  $week[6] = "土";
  echo $week[date("w")];
?>
曜日です。</p>

</body>
</html>
