
<!DOCTYPE html>
<html lang="ja">
<head>
    <title>Document</title>
</head>
<body>


<?php
$now = getdate(); // 現在時刻の情報を持った配列を作成
$month = $now['mon']; // 今月
$today = $now['mday']; // 今日
$year = $now['year']; // 今年
 
// 「来年の今日」の日時情報を持った配列を作成
$nextyear = getdate( mktime( 0, 0, 0, $month, $today, $year+1 ) );
 
// 現在時刻の方の配列情報出力
echo '<pre>';
print_r($now);
echo '</pre>';
 
// 今日の日付と時間を出力
echo '今日は';
echo $year.'年'.$month.'月'.$today.'日 ';
echo $now['minutes'].'分';
echo $now['minutes'].'分';
echo $now['hours'].'時';
echo $now['minutes'].'分';
echo $now['seconds'].'秒';
echo "<br />\n";
echo '来年の今日の曜日は'.$nextyear['weekday'];
?>

<?php
  $num = rand(0, 1);
  if ($num == 0) {
    echo "今日の運勢は大吉です。";
  } else {
    echo "今日の運勢は凶です。";
  }?>


<form action="vote.php" method="post">
<table>
  <tr>
    <td>小泉首相</td>
    <td><input type="radio" name="vote" value="0"></td>
  </tr>
  <tr>
    <td>ビンラディン</td>
    <td><input type="radio" name="vote" value="1"></td>
  </tr>
  <tr>
    <td>愛子さま</td>
    <td><input type="radio" name="vote" value="2"></td>
  </tr>
  <tr>
    <td>その他</td>
    <td><input type="radio" name="vote" value="3"></td>
  </tr>
</table>
<p><input type="submit" value="投票"></p>
</form>
<p>
あなたは
<?php
  echo "<img src=\"$c3.jpg\" alt=\"$c3\">";
  echo "<img src=\"$c2.jpg\" alt=\"$c2\">";
  echo "<img src=\"$c1.jpg\" alt=\"$c1\">";
  echo "<img src=\"$c0.jpg\" alt=\"$c0\">";
?>
人目のお客様です。
</p>

<?php
  date_default_timezone_set('Asia/Tokyo');
?>
    
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
