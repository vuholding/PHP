# PHP
define('ROOT_DIR', $_SERVER['DOCUMENT_ROOT']);

require_once ROOT_DIR . '/libs/db.php';
$query = R::getRow("SELECT * FROM pages WHERE pagealias='".$url."' AND pagepublish='Y' LIMIT 1");


$today = date("Y-m-d H:i:s");
echo $today;
//2018-07-24 18:12:08
//18:15:59
$todayhors = date("H:i:s");
echo '<br>'. $todayhors;
if ($todayhors >= '18:20:00' && $todayhors <= '18:21:00' ){
    echo '<br>go';
}else{
    echo '<br>no';
}

if ($today >= '2018-07-24 18:24:00' && $today <= '2018-07-24 18:25:00' ){
    echo '<br>go foo';
}else{
    echo '<br>no fo';
}
