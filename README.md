
<!DOCTYPE html>
<html lang="en">
<head>
    <title>Document</title>
</head>
<body>
    
<form action="ques.php" method="post">
<p>身長: <input name="height" size="5"> cm</p>
<p>体重: <input name="weight" size="5"> kg</p>
<p><input type="submit" value="送る">
<input type="reset" value="クリア"></p>
</form>


<h1>いま何時？</h1>

<p>いま
<?php date_default_timezone_set('Asia/Tokyo');
echo date("Y 年 m 月 d 日 H 時 i 分 s 秒"); ?>
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


<p>
<?php
  date_default_timezone_set('Asia/Tokyo');
  $h = date("H");
  if ($h < 10)
    echo "おはようございます";
  elseif ($h < 18)
    echo "こんにちは";
  else
    echo "こんばんは";
?>
</p>
<p>
<?php
  date_default_timezone_set('Asia/Tokyo');
  $h = date("H");
  if ($h < 10) {
    echo "おはようございます";
  } elseif ($h < 18) {
    echo "こんにちは";
  } else {
    echo "こんばんは";
  }
?>
</p>


<p>このページは
<?php echo date("Y 年 m 月 d 日 H 時 i 分 s 秒", filemtime("time.php")); ?>
に更新されました。</p>

</body>
</html>
