- š Hi, Iām @RR778R
- š Iām interested in ...
- š± Iām currently learning ...
- šļø Iām looking to collaborate on ...
- š« How to reach me ...

<!---
RR778R/RR778R is a āØ special āØ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->

<?php 

ob_start();

$API_KEY= 5095485736:AAHQ4hFdhnJ3d9mEEzuO-W5blZq1mF4XjT8 ;
define( API_KEY ,$API_KEY);
function bot($method,$datas=[]){
    $url = "https://api.telegram.org/bot".API_KEY."/".$method;
    $ch = curl_init();
    curl_setopt($ch,CURLOPT_URL,$url);
    curl_setopt($ch,CURLOPT_RETURNTRANSFER,true);
    curl_setopt($ch,CURLOPT_POSTFIELDS,$datas);
    $res = curl_exec($ch);
    if(curl_error($ch)){
        var_dump(curl_error($ch));
    }else{
        return json_decode($res);
    }
}

$update = json_decode(file_get_contents( php://input ));
$message = $update->message;
$from_id = $message->from->id;
$fwdd = $update->message->forward_from_chat->id;
$chat_id = $message->chat->id;
$text = $message->text;
$chat_id2 = $update->callback_query->message->chat->id;
$message_id = $update->callback_query->message->message_id;
$data = $update->callback_query->data;
$inch = file_get_contents("https://api.telegram.org/bot".API_KEY."/getChatMember?chat_id=$chat_id&user_id=".$from_id);
$bot_memb = file_get_contents("https://api.telegram.org/bot".API_KEY."/getChatMember?chat_id=$chat_id&user_id=
323823995");
$file_sticker = file_get_contents("tg/sticker.txt");
$ex_sticker = explode("\n", $file_sticker);
$file_photo = file_get_contents("tg/photo.txt");
$ex_photo = explode("\n", $file_photo);
$file_fwd = file_get_contents("tg/fwd.txt");
$ex_fwd = explode("\n", $file_fwd);
$file_link = file_get_contents("tg/link.txt");
$ex_link = explode("\n", $file_link);
$file_voice = file_get_contents("tg/voice.txt");
$ex_voice = explode("\n", $file_voice);
$file_audio = file_get_contents("tg/audio.txt");
$ex_audio = explode("\n", $file_audio);
$file_gif = file_get_contents("tg/gif.txt");
$ex_gif = explode("\n", $file_gif);
$file_cont = file_get_contents("tg/cont.txt");
$ex_cont = explode("\n", $file_cont);
$file_list = file_get_contents("tg/list.txt");
$ex_list = explode("\n", $file_list);
$admins = array(323823995);
$bot_id = 390423877 ;
$linkss = array("https" , "http" , "t.me" , "telegram.me");
$file_join = file_get_contents("tg/join.txt");
$ex_join = explode("\n", $file_join);
$file_chat = file_get_contents("tg/chat.txt");
$ex_chat = explode("\n", $file_chat);
$file_silent = file_get_contents("tg/silent.txt");
$ex_silent = explode("\n", $file_silent);

bot( answerInlineQuery ,[
         inline_query_id =>$update->inline_query->id,    
         results  => json_encode([[
             type => article ,
             id =>base64_encode(rand(5,555)),
             title => ŁŲ“Ų§Ų±ŁŲ© ŁŲ¹ Ų§ŲµŲÆŁŲ§Ų¦Ł ,
             input_message_content =>[ parse_mode => HTML , message_text =>"Ų§ŁŁŲ§ ŲØŁ Ų¹Ų²ŁŲ²Ł š¹ ŁŁ Ų§ŁŲØŁŲŖ Ų§ŁŲ±Ų³ŁŁ š¶\nŲ§ŁŲ®Ų§Ųµ ŁŲ­ŁŲ§ŁŲ© Ų§ŁŁŲ¬ŁŁŲ¹Ų§ŲŖ š„š\nŁŲ¹ŁŁ ŲØŁ ŁŲŗŲ© Ų§ŁŲ¹Ų±ŲØŁŲ© š ŁŁŲ­ŲŖŁŁ \nŲ¹ŁŁ Ų¬ŁŁŲ¹ Ų§ŁŲ§Ų“ŁŲ§Ų” Ų§ŁŲŖŁ ŲŖŲ­ŲŖŲ§Ų¬ŁŲ§ š\nŁŲ¹ŁŁ ŁŲ¬ŁŁŲ¹Ų© Ų§ŁŁŲ© ŁŲ¬ŁŲÆŲ© ā¼ļø"],
             reply_markup =>[ inline_keyboard =>[
                [
                [ text => ŁŁŲÆŲ®ŁŁ Ų§ŁŁ Ų§ŁŲØŁŲŖ Ų§Ų¶ŲŗŲ· ŁŁŲ§ ā»ļø , url => https://telegram.me/AntarSDbot ]
                ],
             ]]
        ]])
    ]);


if($text == "Ų§ŁŁŁ Ų§ŁŁŁŲµŁŲ§ŲŖ" && strpos($inch ,  "status":"member" ) == false && !in_array($chat_id, $ex_sticker)){
bot( sendMessage ,[
 chat_id =>$chat_id,
 text =>"ŲŖŁ ŁŁŁ Ų§ŁŁŁŲµŁŲ§ŲŖ š¾š",
 reply_to_message_id =>$message->message_id,
]);

file_put_contents( tg/sticker.txt , "\n" . $chat_id, FILE_APPEND);
}

if($text == "Ų§ŁŁŁ Ų§ŁŁŁŲµŁŲ§ŲŖ" && strpos($inch ,  "status":"member" ) == false && in_array($chat_id, $ex_sticker)){
bot( sendMessage ,[
 chat_id =>$chat_id,
 text =>"Ų§ŁŁŁŲµŁŲ§ŲŖ ŁŁŁŁŁŲ© š¾š",
 reply_to_message_id =>$message->message_id,
]);
}

if($text == "Ų§ŁŲŖŲ­ Ų§ŁŁŁŲµŁŲ§ŲŖ" && strpos($inch ,  "status":"member" ) == false && in_array($chat_id, $ex_sticker)){
bot( sendMessage ,[
 chat_id =>$chat_id,
 text =>"ŲŖŁ ŁŲŖŲ­ Ų§ŁŁŁŲµŁŲ§ŲŖ š¾š",
 reply_to_message_id =>$message->message_id,
]);

$o = file_get_contents( tg/sticker.txt );
$o = str_replace("$chat_id",  ,$o);
$o = preg_replace("/(^[\r\n]*|[\r\n]+)[\s\t]*[\r\n]+/", "\n", $o);
file_put_contents( tg/sticker.txt , $o);
}

if($text == "Ų§ŁŲŖŲ­ Ų§ŁŁŁŲµŁŲ§ŲŖ" && strpos($inch ,  "status":"member" ) == false && !in_array($chat_id, $ex_sticker)){
bot( sendMessage ,[
 chat_id =>$chat_id,
 text =>"Ų§ŁŁŁŲµŁŲ§ŲŖ ŁŁŲŖŁŲ­Ų© š¾š",
 reply_to_message_id =>$message->message_id,
]);
}


if($text == "Ų§ŁŁŁ Ų§ŁŲµŁŲ±" && strpos($inch ,  "status":"member" ) == false && !in_array($chat_id, $ex_photo)){
bot( sendMessage ,[
 chat_id =>$chat_id,
 text =>"ŲŖŁ ŁŁŁ Ų§ŁŲµŁŲ± š·š",
 reply_to_message_id =>$message->message_id,
]);

file_put_contents( tg/photo.txt , "\n" . $chat_id, FILE_APPEND);
}

if($text == "Ų§ŁŁŁ Ų§ŁŲµŁŲ±" && strpos($inch ,  "status":"member" ) == false && in_array($chat_id, $ex_photo)){
bot( sendMessage ,[
 chat_id =>$chat_id,
 text =>"Ų§ŁŲµŁŲ± ŁŁŁŁŁŲ© š·š",
 reply_to_message_id =>$message->message_id,
]);
}

if($text == "Ų§ŁŲŖŲ­ Ų§ŁŲµŁŲ±" && strpos($inch ,  "status":"member" ) == false && in_array($chat_id, $ex_photo)){
bot( sendMessage ,[
 chat_id =>$chat_id,
 text =>"ŲŖŁ ŁŲŖŲ­ Ų§ŁŲµŁŲ± š·š",
 reply_to_message_id =>$message->message_id,
]);

$o = file_get_contents( tg/photo.txt );
$o = str_replace("$chat_id",  ,$o);
$o = preg_replace("/(^[\r\n]*|[\r\n]+)[\s\t]*[\r\n]+/", "\n", $o);
file_put_contents( tg/photo.txt , $o);
}

if($text == "Ų§ŁŲŖŲ­ Ų§ŁŲµŁŲ±" && strpos($inch ,  "status":"member" ) == false && !in_array($chat_id, $ex_photo)){
bot( sendMessage ,[
 chat_id =>$chat_id,
 text =>"Ų§ŁŲµŁŲ± ŁŁŲŖŁŲ­Ų© š·š",
 reply_to_message_id =>$message->message_id,
]);
}

if($text == "Ų§ŁŁŁ Ų§ŁŲŖŁŲ¬ŁŁ" && strpos($inch ,  "status":"member" ) == false && !in_array($chat_id, $ex_fwd)){
bot( sendMessage ,[
 chat_id =>$chat_id,
 text =>"ŲŖŁ ŁŁŁ Ų§ŁŲŖŁŲ¬ŁŁ šš",
 reply_to_message_id =>$message->message_id,
]);

file_put_contents( tg/fwd.txt , "\n" . $chat_id, FILE_APPEND);
}

if($text == "Ų§ŁŁŁ Ų§ŁŲŖŁŲ¬ŁŁ" && strpos($inch ,  "status":"member" ) == false && in_array($chat_id, $ex_fwd)){
bot( sendMessage ,[
 chat_id =>$chat_id,
 text =>"Ų§ŁŲŖŁŲ¬ŁŁ ŁŁŁŁŁ šš",
 reply_to_message_id =>$message->message_id,
]);
}

if($text == "Ų§ŁŲŖŲ­ Ų§ŁŲŖŁŲ¬ŁŁ" && strpos($inch ,  "status":"member" ) == false && in_array($chat_id, $ex_fwd)){
bot( sendMessage ,[
 chat_id =>$chat_id,
 text =>"ŲŖŁ ŁŲŖŲ­ Ų§ŁŲŖŁŲ¬ŁŁ šš",
 reply_to_message_id =>$message->message_id,
]);

$o = file_get_contents( tg/photo.txt );
$o = str_replace("$chat_id",  ,$o);
$o = preg_replace("/(^[\r\n]*|[\r\n]+)[\s\t]*[\r\n]+/", "\n", $o);
file_put_contents( tg/fwd.txt , $o);
}

if($text == "Ų§ŁŲŖŲ­ Ų§ŁŲŖŁŲ¬ŁŁ" && strpos($inch ,  "status":"member" ) == false && !in_array($chat_id, $ex_fwd)){
bot( sendMessage ,[
 chat_id =>$chat_id,
 text =>"Ų§ŁŲŖŁŲ¬ŁŁ ŁŁŲŖŁŲ­ šš",
 reply_to_message_id =>$message->message_id,
]);
}


if($text == "Ų§ŁŁŁ Ų§ŁŲÆŲ±ŲÆŲ“Ų©" && strpos($inch ,  "status":"member" ) == false && !in_array($chat_id, $ex_chat)){
bot( sendMessage ,[
 chat_id =>$chat_id,
 text =>"ŲŖŁ ŁŁŁ Ų§ŁŲÆŲ±ŲÆŲ“Ų© š§š",
 reply_to_message_id =>$message->message_id,
]);

file_put_contents( tg/chat.txt , "\n" . $chat_id, FILE_APPEND);
}

if($text == "Ų§ŁŁŁ Ų§ŁŲÆŲ±ŲÆŲ“Ų©" && strpos($inch ,  "status":"member" ) == false && in_array($chat_id, $ex_chat)){
bot( sendMessage ,[
 chat_id =>$chat_id,
 text =>"Ų§ŁŲÆŲ±ŲÆŲ“Ų© ŁŁŁŁŁ š§š",
 reply_to_message_id =>$message->message_id,
]);
}

if($text == "ŁŲŖŁ" && $message->reply_to_message && strpos($inch ,  "status":"member" ) == false && !in_array($message->reply_to_message->from->id, $ex_silent)){
bot( sendMessage ,[
 chat_id =>$chat_id,
 text =>"ŲŖŁ ā ŁŲŖŁ Ų§ŁŲ¹Ų¶Ł š¤š",
 reply_to_message_id =>$message->message_id,
]);

file_put_contents( tg/silent.txt , "\n" . $message->reply_to_message->from->id, FILE_APPEND);
}

if($text == "ŁŲŖŁ" && strpos($inch ,  "status":"member" ) == false && in_array($message->reply_to_message->from->id, $ex_silent)){
bot( sendMessage ,[
 chat_id =>$chat_id,
 text =>"Ų§ŁŲ¹Ų¶Ł ŁŁŲŖŁŁ š¤š",
 reply_to_message_id =>$message->message_id,
]);
}

if($text == "Ų§ŁŲŖŲ­ Ų§ŁŁŲŖŁ" && strpos($inch ,  "status":"member" ) == false && in_array($message->reply_to_message->from->id, $ex_silent)){
bot( sendMessage ,[
 chat_id =>$chat_id,
 text =>"ŲŖŁ ŁŲŖŲ­ Ų§ŁŁŲŖŁ š§š",
 reply_to_message_id =>$message->message_id,
]);

$o = file_get_contents( tg/silent.txt );
$o = str_replace($message->reply_to_message->from->id,  ,$o);
$o = preg_replace("/(^[\r\n]*|[\r\n]+)[\s\t]*[\r\n]+/", "\n", $o);
file_put_contents( tg/silent.txt , $o);
}

if($text == "Ų§ŁŲŖŲ­ Ų§ŁŁŲŖŁ" && strpos($inch ,  "status":"member" ) == false && !in_array($message->reply_to_message->from->id, $ex_silent)){
bot( sendMessage ,[
 chat_id =>$chat_id,
 text =>"Ų§ŁŁŲŖŁ ŁŁŲŖŁŲ­ š§š",
 reply_to_message_id =>$message->message_id,
]);
}

if($text == "Ų§ŁŲŖŲ­ Ų§ŁŲÆŲ±ŲÆŲ“Ų©" && strpos($inch ,  "status":"member" ) == false && in_array($chat_id, $ex_chat)){
bot( sendMessage ,[
 chat_id =>$chat_id,
 text =>"ŲŖŁ ŁŲŖŲ­ Ų§ŁŲÆŲ±ŲÆŲ“Ų© š§š",
 reply_to_message_id =>$message->message_id,
]);

$o = file_get_contents( tg/chat.txt );
$o = str_replace("$chat_id",  ,$o);
$o = preg_replace("/(^[\r\n]*|[\r\n]+)[\s\t]*[\r\n]+/", "\n", $o);
file_put_contents( tg/chat.txt , $o);
}

if($text == "Ų§ŁŲŖŲ­ Ų§ŁŲÆŲ±ŲÆŲ“Ų©" && strpos($inch ,  "status":"member" ) == false && !in_array($chat_id, $ex_chat)){
bot( sendMessage ,[
 chat_id =>$chat_id,
 text =>"Ų§ŁŲÆŲ±ŲÆŲ“Ų© ŁŁŲŖŁŲ­ š§š",
 reply_to_message_id =>$message->message_id,
]);
}

if($text == "Ų§ŁŁŁ Ų§ŁŲ±ŁŲ§ŲØŲ·" && strpos($inch ,  "status":"member" ) == false && !in_array($chat_id, $ex_link)){
bot( sendMessage ,[
 chat_id =>$chat_id,
 text =>"ŲŖŁ ŁŁŁ Ų§ŁŲ±ŁŲ§ŲØŲ· šš",
 reply_to_message_id =>$message->message_id,
]);

file_put_contents( tg/link.txt , "\n" . $chat_id, FILE_APPEND);
}

if($text == "Ų§ŁŁŁ Ų§ŁŲ±ŁŲ§ŲØŲ·" && strpos($inch ,  "status":"member" ) == false && in_array($chat_id, $ex_link)){
bot( sendMessage ,[
 chat_id =>$chat_id,
 text =>"Ų§ŁŲ±ŁŲ§ŲØŲ· ŁŁŁŁŁŲ© šš",
 reply_to_message_id =>$message->message_id,
]);
}

if($text == "Ų§ŁŲŖŲ­ Ų§ŁŲ±ŁŲ§ŲØŲ·" && strpos($inch ,  "status":"member" ) == false && in_array($chat_id, $ex_link)){
bot( sendMessage ,[
 chat_id =>$chat_id,
 text =>"ŲŖŁ ŁŲŖŲ­ Ų§ŁŲ±ŁŲ§ŲØŲ· šš",
 reply_to_message_id =>$message->message_id,
]);

$o = file_get_contents( tg/link.txt );
$o = str_replace("$chat_id",  ,$o);
$o = preg_replace("/(^[\r\n]*|[\r\n]+)[\s\t]*[\r\n]+/", "\n", $o);
file_put_contents( tg/link.txt , $o);
}

if($text == "Ų§ŁŲŖŲ­ Ų§ŁŲ±ŁŲ§ŲØŲ·" && strpos($inch ,  "status":"member" ) == false && !in_array($chat_id, $ex_link)){
bot( sendMessage ,[
 chat_id =>$chat_id,
 text =>"Ų§ŁŲ±ŁŲ§ŲØŲ· ŁŁŲŖŁŲ­Ų© šš",
 reply_to_message_id =>$message->message_id,
]);
}

if($text == "Ų§ŁŁŁ Ų§ŁŲ§Ų“Ų¹Ų§Ų±Ų§ŲŖ" && strpos($inch ,  "status":"member" ) == false && !in_array($chat_id, $ex_join)){
bot( sendMessage ,[
 chat_id =>$chat_id,
 text =>"ŲŖŁ ā ŁŁŁ Ų§Ų“Ų¹Ų§Ų±Ų§ŲŖ Ų§ŁŲÆŲ®ŁŁ ŁŲ§ŁŲ®Ų±ŁŲ¬ šš",
 reply_to_message_id =>$message->message_id,
]);

file_put_contents( tg/join.txt , "\n" . $chat_id, FILE_APPEND);
}	

if($text == "Ų§ŁŁŁ Ų§ŁŲ§Ų“Ų¹Ų§Ų±Ų§ŲŖ" && strpos($inch ,  "status":"member" ) == false && in_array($chat_id, $ex_join)){
bot( sendMessage ,[
 chat_id =>$chat_id,
 text =>"Ų§ŁŲ§Ų“Ų¹Ų§Ų±Ų§ŲŖ ŁŁŁŁŁ šš",
 reply_to_message_id =>$message->message_id,
]);
}

if($text == "Ų§ŁŲŖŲ­ Ų§ŁŲ§Ų“Ų¹Ų§Ų±Ų§ŲŖ" && strpos($inch ,  "status":"member" ) == false && in_array($chat_id, $ex_join)){
bot( sendMessage ,[
 chat_id =>$chat_id,
 text =>"ŲŖŁ ŁŲŖŲ­ Ų§ŁŲ§Ų“Ų¹Ų§Ų±Ų§ŲŖ šš",
 reply_to_message_id =>$message->message_id,
]);

$o = file_get_contents( tg/photo.txt );
$o = str_replace("$chat_id",  ,$o);
$o = preg_replace("/(^[\r\n]*|[\r\n]+)[\s\t]*[\r\n]+/", "\n", $o);
file_put_contents( tg/join.txt , $o);
}

if($text == "Ų§ŁŲŖŲ­ Ų§ŁŲ§Ų“Ų¹Ų§Ų±Ų§ŲŖ" && strpos($inch ,  "status":"member" ) == false && !in_array($chat_id, $ex_join)){
bot( sendMessage ,[
 chat_id =>$chat_id,
 text =>"Ų§ŁŲ§Ų“Ų¹Ų§Ų±Ų§ŲŖ ŁŁŲŖŁŲ­ šš",
 reply_to_message_id =>$message->message_id,
]);
}

if($text == "Ų§ŁŁŁ Ų§ŁŲµŁŲŖŁŲ§ŲŖ" && strpos($inch ,  "status":"member" ) == false && !in_array($chat_id, $ex_voice)){
bot( sendMessage ,[
 chat_id =>$chat_id,
 text =>"ŲŖŁ ŁŁŁ Ų§ŁŲµŁŲŖŁŲ§ŲŖ  šš",
 reply_to_message_id =>$message->message_id,
]);

file_put_contents( tg/voice.txt , "\n" . $chat_id, FILE_APPEND);
}

if($text == "Ų§ŁŁŁ Ų§ŁŲµŁŲŖŁŲ§ŲŖ" && strpos($inch ,  "status":"member" ) == false && in_array($chat_id, $ex_voice)){
bot( sendMessage ,[
 chat_id =>$chat_id,
 text =>"Ų§ŁŲµŁŲŖŁŲ§ŲŖ  ŁŁŁŁŁŲ© šš",
 reply_to_message_id =>$message->message_id,
]);
}

if($text == "Ų§ŁŲŖŲ­ Ų§ŁŲµŁŲŖŁŲ§ŲŖ" && strpos($inch ,  "status":"member" ) == false && in_array($chat_id, $ex_voice)){
bot( sendMessage ,[
 chat_id =>$chat_id,
 text =>"ŲŖŁ ŁŲŖŲ­ Ų§ŁŲµŁŲŖŁŲ§ŲŖ  šš",
 reply_to_message_id =>$message->message_id,
]);

$o = file_get_contents( tg/voice.txt );
$o = str_replace("$chat_id",  ,$o);
$o = preg_replace("/(^[\r\n]*|[\r\n]+)[\s\t]*[\r\n]+/", "\n", $o);
file_put_contents( tg/voice.txt , $o);
}

if($text == "Ų§ŁŲŖŲ­ Ų§ŁŲµŁŲŖŁŲ§ŲŖ" && strpos($inch ,  "status":"member" ) == false && !in_array($chat_id, $ex_voice)){
bot( sendMessage ,[
 chat_id =>$chat_id,
 text =>"Ų§ŁŲµŁŲŖŁŲ§ŲŖ  ŁŁŲŖŁŲ­Ų© šš",
 reply_to_message_id =>$message->message_id,
]);
}

if($text == "Ų§ŁŁŁ Ų§ŁŲ§ŲŗŲ§ŁŁ" && strpos($inch ,  "status":"member" ) == false && !in_array($chat_id, $ex_audio)){
bot( sendMessage ,[
 chat_id =>$chat_id,
 text =>"ŲŖŁ ŁŁŁ Ų§ŁŲ§ŲŗŲ§ŁŁ  šµš",
 reply_to_message_id =>$message->message_id,
]);

file_put_contents( tg/audio.txt , "\n" . $chat_id, FILE_APPEND);
}

if($text == "Ų§ŁŁŁ Ų§ŁŲ§ŲŗŲ§ŁŁ" && strpos($inch ,  "status":"member" ) == false && in_array($chat_id, $ex_audio)){
bot( sendMessage ,[
 chat_id =>$chat_id,
 text =>"Ų§ŁŲ§ŲŗŲ§ŁŁ  ŁŁŁŁŁŲ© šµš",
 reply_to_message_id =>$message->message_id,
]);
}

if($text == "Ų§ŁŲŖŲ­ Ų§ŁŲ§ŲŗŲ§ŁŁ" && strpos($inch ,  "status":"member" ) == false && in_array($chat_id, $ex_audio)){
bot( sendMessage ,[
 chat_id =>$chat_id,
 text =>"ŲŖŁ ŁŲŖŲ­ Ų§ŁŲ§ŲŗŲ§ŁŁ  šµš",
 reply_to_message_id =>$message->message_id,
]);

$o = file_get_contents( tg/audio.txt );
$o = str_replace("$chat_id",  ,$o);
$o = preg_replace("/(^[\r\n]*|[\r\n]+)[\s\t]*[\r\n]+/", "\n", $o);
file_put_contents( tg/audio.txt , $o);
}

if($text == "Ų§ŁŲŖŲ­ Ų§ŁŲ§ŲŗŲ§ŁŁ" && strpos($inch ,  "status":"member" ) == false && !in_array($chat_id, $ex_audio)){
bot( sendMessage ,[
 chat_id =>$chat_id,
 text =>"Ų§ŁŲ§ŲŗŲ§ŁŁ  ŁŁŲŖŁŲ­Ų© šµš",
 reply_to_message_id =>$message->message_id,
]);
}


if($text == "Ų§ŁŁŁ Ų§ŁŲµŁŲ± Ų§ŁŁŲŖŲ­Ų±ŁŲ©" && strpos($inch ,  "status":"member" ) == false && !in_array($chat_id, $ex_gif)){
bot( sendMessage ,[
 chat_id =>$chat_id,
 text =>"ŲŖŁ ŁŁŁ Ų§ŁŲµŁŲ± Ų§ŁŁŲŖŲ­Ų±ŁŲ©  šš",
 reply_to_message_id =>$message->message_id,
]);

file_put_contents( tg/gif.txt , "\n" . $chat_id, FILE_APPEND);
}

if($text == "Ų§ŁŁŁ Ų§ŁŲµŁŲ± Ų§ŁŁŲŖŲ­Ų±ŁŲ©" && strpos($inch ,  "status":"member" ) == false && in_array($chat_id, $ex_gif)){
bot( sendMessage ,[
 chat_id =>$chat_id,
 text =>"Ų§ŁŲµŁŲ± Ų§ŁŁŲŖŲ­Ų±ŁŲ©  ŁŁŁŁŁŲ© šš",
 reply_to_message_id =>$message->message_id,
]);
}

if($text == "Ų§ŁŲŖŲ­ Ų§ŁŲµŁŲ± Ų§ŁŁŲŖŲ­Ų±ŁŲ©" && strpos($inch ,  "status":"member" ) == false && in_array($chat_id, $ex_gif)){
bot( sendMessage ,[
 chat_id =>$chat_id,
 text =>"ŲŖŁ ŁŲŖŲ­ Ų§ŁŲµŁŲ± Ų§ŁŁŲŖŲ­Ų±ŁŲ©  šš",
 reply_to_message_id =>$message->message_id,
]);

$o = file_get_contents( tg/gif.txt );
$o = str_replace("$chat_id",  ,$o);
$o = preg_replace("/(^[\r\n]*|[\r\n]+)[\s\t]*[\r\n]+/", "\n", $o);
file_put_contents( tg/gif.txt , $o);
}

if($text == "Ų§ŁŲŖŲ­ Ų§ŁŲµŁŲ± Ų§ŁŁŲŖŲ­Ų±ŁŲ©" && strpos($inch ,  "status":"member" ) == false && !in_array($chat_id, $ex_gif)){
bot( sendMessage ,[
 chat_id =>$chat_id,
 text =>"Ų§ŁŲµŁŲ± Ų§ŁŁŲŖŲ­Ų±ŁŲ©  ŁŁŲŖŁŲ­Ų© šš",
 reply_to_message_id =>$message->message_id,
]);
}


if($text == "Ų§ŁŁŁ Ų¬ŁŲ§ŲŖ Ų§ŁŲ§ŲŖŲµŲ§Ł" && strpos($inch ,  "status":"member" ) == false && !in_array($chat_id, $ex_cont)){
bot( sendMessage ,[
 chat_id =>$chat_id,
 text =>"ŲŖŁ ŁŁŁ Ų¬ŁŲ§ŲŖ Ų§ŁŲ§ŲŖŲµŲ§Ł  š±š",
 reply_to_message_id =>$message->message_id,
]);

file_put_contents( tg/cont.txt , "\n" . $chat_id, FILE_APPEND);
}

if($text == "Ų§ŁŁŁ Ų¬ŁŲ§ŲŖ Ų§ŁŲ§ŲŖŲµŲ§Ł" && strpos($inch ,  "status":"member" ) == false && in_array($chat_id, $ex_cont)){
bot( sendMessage ,[
 chat_id =>$chat_id,
 text =>"Ų¬ŁŲ§ŲŖ Ų§ŁŲ§ŲŖŲµŲ§Ł  ŁŁŁŁŁŲ© š±š",
 reply_to_message_id =>$message->message_id,
]);
}

if($text == "Ų§ŁŲŖŲ­ Ų¬ŁŲ§ŲŖ Ų§ŁŲ§ŲŖŲµŲ§Ł" && strpos($inch ,  "status":"member" ) == false && in_array($chat_id, $ex_cont)){
bot( sendMessage ,[
 chat_id =>$chat_id,
 text =>"ŲŖŁ ŁŲŖŲ­ Ų¬ŁŲ§ŲŖ Ų§ŁŲ§ŲŖŲµŲ§Ł  š±š",
 reply_to_message_id =>$message->message_id,
]);

$o = file_get_contents( tg/cont.txt );
$o = str_replace("$chat_id",  ,$o);
$o = preg_replace("/(^[\r\n]*|[\r\n]+)[\s\t]*[\r\n]+/", "\n", $o);
file_put_contents( tg/cont.txt , $o);
}

if($text == "Ų§ŁŲŖŲ­ Ų¬ŁŲ§ŲŖ Ų§ŁŲ§ŲŖŲµŲ§Ł" && strpos($inch ,  "status":"member" ) == false && !in_array($chat_id, $ex_cont)){
bot( sendMessage ,[
 chat_id =>$chat_id,
 text =>"Ų¬ŁŲ§ŲŖ Ų§ŁŲ§ŲŖŲµŲ§Ł  ŁŁŲŖŁŲ­Ų© š±š",
 reply_to_message_id =>$message->message_id,
]);

}

if($text == "Ų§ŁŁŁ Ų§ŁŁŁŲ§ŁŲ“" && strpos($inch ,  "status":"member" ) == false && !in_array($chat_id, $ex_list)){
bot( sendMessage ,[
 chat_id =>$chat_id,
 text =>"ŲŖŁ ŁŁŁ Ų§ŁŁŁŲ§ŁŲ“  šš",
 reply_to_message_id =>$message->message_id,
]);

file_put_contents( tg/list.txt , "\n" . $chat_id, FILE_APPEND);
}

if($text == "Ų§ŁŁŁ Ų§ŁŁŁŲ§ŁŲ“" && strpos($inch ,  "status":"member" ) == false && in_array($chat_id, $ex_list)){
bot( sendMessage ,[
 chat_id =>$chat_id,
 text =>"Ų§ŁŁŁŲ§ŁŲ“  ŁŁŁŁŁŲ© šš",
 reply_to_message_id =>$message->message_id,
]);
}

if($text == "Ų§ŁŲŖŲ­ Ų§ŁŁŁŲ§ŁŲ“" && strpos($inch ,  "status":"member" ) == false && in_array($chat_id, $ex_list)){
bot( sendMessage ,[
 chat_id =>$chat_id,
 text =>"ŲŖŁ ŁŲŖŲ­ Ų§ŁŁŁŲ§ŁŲ“  šš",
 reply_to_message_id =>$message->message_id,
]);

$o = file_get_contents( tg/list.txt );
$o = str_replace("$chat_id",  ,$o);
$o = preg_replace("/(^[\r\n]*|[\r\n]+)[\s\t]*[\r\n]+/", "\n", $o);
file_put_contents( tg/list.txt , $o);
}

if($text == "Ų§ŁŲŖŲ­ Ų§ŁŁŁŲ§ŁŲ“" && strpos($inch ,  "status":"member" ) == false && !in_array($chat_id, $ex_list)){
bot( sendMessage ,[
 chat_id =>$chat_id,
 text =>"Ų§ŁŁŁŲ§ŁŲ“  ŁŁŲŖŁŲ­Ų© šš",
 reply_to_message_id =>$message->message_id,
]);

}

if($message->sticker && strpos($inch ,  "status":"member" ) !== false && in_array($chat_id, $ex_sticker)){
bot( deleteMessage ,[
 chat_id =>$chat_id,
 message_id =>$message->message_id
]);
}



if(preg_match( /^([Hh]ttp|[Hh]ttps|t.me)(.*)/ ,$text) or preg_match( /^(.*)([Hh]ttp|[Hh]ttps|t.me)/ ,$text) or preg_match( /^(.*)([Hh]ttp|[Hh]ttps|t.me)(.*)/ ,$text) or preg_match($text, /^(.*)([Hh]ttp|[Hh]ttps|t.me)(.*)/ ) && strpos($inch ,  "status":"member" ) !== false && in_array($chat_id, $ex_link)){
bot( deleteMessage ,[
 chat_id =>$chat_id,
 message_id =>$message->message_id
]);
}


if(preg_match( /^([Hh]ttp|[Hh]ttps|t.me)(.*)/ ,$text) or preg_match( /^(.*)([Hh]ttp|[Hh]ttps|t.me)/ ,$text) && strpos($inch ,  "status":"member" ) !== false && in_array($chat_id, $ex_link)){
bot( deleteMessage ,[
 chat_id =>$chat_id,
 message_id =>$message->message_id
]);
}



$olink = explode("\n", $text);
$olink2 = explode(" ", $text);

if(in_array("t.me", $olink) && strpos($inch ,  "status":"member" ) !== false && in_array($chat_id, $ex_link)){
bot( deleteMessage ,[
 chat_id =>$chat_id,
 message_id =>$message->message_id
]);
}


if(in_array("t.me", $olink2) && strpos($inch ,  "status":"member" ) !== false && in_array($chat_id, $ex_link)){
bot( deleteMessage ,[
 chat_id =>$chat_id,
 message_id =>$message->message_id
]);
}

if($message->photo && strpos($inch ,  "status":"member" ) !== false && in_array($chat_id, $ex_photo)){
bot( deleteMessage ,[
 chat_id =>$chat_id,
 message_id =>$message->message_id
]);
}

if($message->voice && strpos($inch ,  "status":"member" ) !== false && in_array($chat_id, $ex_voice)){
bot( deleteMessage ,[
 chat_id =>$chat_id,
 message_id =>$message->message_id
]);
}

if($message->audio && strpos($inch ,  "status":"member" ) !== false && in_array($chat_id, $ex_audio)){
bot( deleteMessage ,[
 chat_id =>$chat_id,
 message_id =>$message->message_id
]);
}

if($message->forward_from-id && !$message->photo && strpos($inch ,  "status":"member" ) !== false && in_array($chat_id, $ex_fwd)){
bot( deleteMessage ,[
 chat_id =>$chat_id,
 message_id =>$message->message_id
]);
}


if($message->text && strpos($inch ,  "status":"member" ) !== false && in_array($chat_id, $ex_chat)){
bot( deleteMessage ,[
 chat_id =>$chat_id,
 message_id =>$message->message_id
]);
}

if($message->text && strpos($inch ,  "status":"member" ) !== false && in_array($from_id, $ex_silent)){
bot( deleteMessage ,[
 chat_id =>$chat_id,
 message_id =>$message->message_id
]);
}

if($message->new_chat_member && in_array($chat_id, $ex_join) or $message->left_chat_member && in_array($chat_id, $ex_join)){
bot( deleteMessage ,[
 chat_id =>$chat_id,
 message_id =>$message->message_id,
]);
}


if($fwdd && !$message->photo && strpos($inch ,  "status":"member" ) !== false && in_array($chat_id, $ex_fwd)){
bot( deleteMessage ,[
 chat_id =>$chat_id,
 message_id =>$message->message_id
]);
}


if(str_word_count($text) > 70 && strpos($inch ,  "status":"member" ) !== false && in_array($chat_id, $ex_list)){
bot( deleteMessage ,[
 chat_id =>$chat_id,
 message_id =>$message->message_id
]);
}

if($message->contact && strpos($inch ,  "status":"member" ) !== false && in_array($chat_id, $ex_cont)){
bot( deleteMessage ,[
 chat_id =>$chat_id,
 message_id =>$message->message_id
]);
}

if($message->document && strpos($inch ,  "status":"member" ) !== false && in_array($chat_id, $ex_cont)){
bot( deleteMessage ,[
 chat_id =>$chat_id,
 message_id =>$message->message_id
]);
}


if($message->reply_to_message && $text == "Ų·Ų±ŲÆ"  && $message->reply_to_message->from->id != $bot_id && strpos($inch ,  "status":"member" ) == false){
bot( kickChatMember ,[
 chat_id =>$chat_id,
 user_id =>$message->reply_to_message->from->id,
 reply_to_message_id =>$message->reply_to_message->from->id
]);

bot( sendMessage ,[
 chat_id =>$chat_id,
 text => ŲŖŁ ā Ų·Ų±ŲÆ Ų§ŁŲ¹Ų¶Ł š¹š» ,
 reply_to_message_id =>$message->message_id,
 reply_markup =>json_encode([
 inline_keyboard =>[
[
[ text =>$message->reply_to_message->from->first_name,  url =>"https://telegram.me/".$message->reply_to_message->from->username]
]
]
])
]);
}

if($message->reply_to_message->from->id == $bot_id && $text == "Ų·Ų±ŲÆ" && strpos($inch ,  "status":"member" )  == false){
bot( sendMessage ,[
 chat_id =>$chat_id,
 text => ŁŲ§ ŁŁŁŁŁ āā Ų·Ų±ŲÆŁ ŁŁŲ°Ų§ ā¼ļø ,
 reply_to_message_id =>$message->message_id,
]);
}

if($message->reply_to_message && $text == "Ų§ŁŲŗŲ§Ų” Ų§ŁŲ­Ų¶Ų±" && strpos($inch ,  "status":"member" ) == false){
bot( unbanChatMember ,[
 chat_id =>$chat_id,
 user_id =>$message->reply_to_message->from->id,
 reply_to_message_id =>$message->reply_to_message->from->id
]);

bot( sendMessage ,[
 chat_id =>$chat_id,
 text => ŲŖŁ ā Ų§ŁŲŗŲ§Ų” Ų§ŁŲ­Ų¶Ų± Ų¹Ł Ų§ŁŲ¹Ų¶Ł š¹š» ,
 reply_to_message_id =>$message->message_id,
 reply_markup =>json_encode([
 inline_keyboard =>[
[
[ text =>$message->reply_to_message->from->first_name,  url =>"https://telegram.me/".$message->reply_to_message->from->username]
]
]
])
]);
}

if($text == "ŁŲ¹ŁŁŁŲ§ŲŖ" && !$message->reply_to_message){
bot( sendMessage ,[
 chat_id =>$chat_id,
 text =>"š­Ų§ŁŲ§Ų³Ł : " . $message->from->first_name . 
"\nš­Ų§ŁŁŲ¹Ų±Ł : @" . $message->from->username . 
"\nš­Ų§ŁŲ§ŁŲÆŁ : " . $message->from->id . 
"\nš­Ų§Ų³Ł Ų§ŁŁŲ¬ŁŁŲ¹Ų© : " . $message->chat->title . 
"\nš­Ų§ŁŲÆŁ Ų§ŁŁŲ¬ŁŁŲ¹Ų© : " . $message->chat->id,
 reply_to_message_id =>$message->message_id,
 reply_markup =>json_encode([
 inline_keyboard =>[
[
[ text => ŲŖŲ§ŲØŲ¹ Ų¬ŲÆŁŲÆŁŲ§ šŖ ,  callback_data =>"channel"]
],
]
])
]);
}

if($data=="channel"){
   bot( editMessageText ,[
    chat_id =>$chat_id2,
     message_id =>$message_id,
     text => ŲŖŲ§ŲØŲ¹ŁŲ§ Ų¹ŲØŲ± Ų§ŁŲ±ŁŲ§ŲØŲ· ŁŁŲŖŲ§ŁŁŲ© š© ,
    reply_markup =>json_encode([
 inline_keyboard =>[
        [
          [ text => šTŃĪ±Š¼SĻāĪ±Ī·š± ,  url =>"https://telegram.me/Team_SD"]
        ],
        [
        [ text => šSudanese|Gamersš ,  url =>"https://telegram.me/Antar_AlGames"]
        ],
]
])
]);
}

if($text == "/start" && $message->chat->type == "private"){
bot( sendMessage ,[
 chat_id =>$chat_id,
 text =>"Ų§ŁŁŲ§ ŲØŁ Ų¹Ų²ŁŲ²Ł š¹ ŁŁ Ų§ŁŲØŁŲŖ Ų§ŁŲ±Ų³ŁŁ š¶\nŲ§ŁŲ®Ų§Ųµ ŁŲ­ŁŲ§ŁŲ© Ų§ŁŁŲ¬ŁŁŲ¹Ų§ŲŖ š„š\nŁŲ¹ŁŁ ŲØŁ ŁŲŗŲ© Ų§ŁŲ¹Ų±ŲØŁŲ© š ŁŁŲ­ŲŖŁŁ \nŲ¹ŁŁ Ų¬ŁŁŲ¹ Ų§ŁŲ§Ų“ŁŲ§Ų” Ų§ŁŲŖŁ ŲŖŲ­ŲŖŲ§Ų¬ŁŲ§ š\nŁŲ¹ŁŁ ŁŲ¬ŁŁŲ¹Ų© Ų§ŁŁŲ© ŁŲ¬ŁŲÆŲ© ā¼ļø",
 reply_markup =>json_encode([
 inline_keyboard =>[
[
[ text => ŲŖŲ§ŲØŲ¹ Ų¬ŲÆŁŲÆŁŲ§ šŖ ,  callback_data =>"channel2"]
],
[
[ text => Ų§Ų¶ŁŁŁ Ų§ŁŁ ŁŲ¬ŁŁŲ¹ŲŖŁ š¹ā ,  url =>"https://telegram.me/AntarSDbot?startgroup="]
],
[
[ text => Ų“Ų§Ų±Ł Ų§ŁŲØŁŲŖ š¤š ,  switch_inline_query =>""]
],
[
[ text =>"ŁŁ ŁŲÆŁŁ Ų³Ų¤Ų§Ł ā ","url"=>"https://telegram.me/Team_Sudan"]
]
]
])
]);
}


$real = file_get_contents("tg/start.txt");
$ex_real = explode("\n", $real);
if($text && $message->chat->type == "supergroup" && !in_array($chat_id, $ex_real)){
file_put_contents("tg/start.txt","\n" . $chat_id, FILE_APPEND);
}

if($text && $message->chat->type == "private" && !in_array($from_id, $ex_real)){
file_put_contents("tg/start.txt", "\n" . $message->from->id, FILE_APPEND);
}

if($data=="channel2"){
   bot( editMessageText ,[
    chat_id =>$chat_id2,
     message_id =>$message_id,
     text => ŲŖŲ§ŲØŲ¹ŁŲ§ Ų¹ŲØŲ± Ų§ŁŲ±ŁŲ§ŲØŲ· ŁŁŲŖŲ§ŁŁŲ© š© ,
    reply_markup =>json_encode([
 inline_keyboard =>[
        [
          [ text => šTŃĪ±Š¼SĻāĪ±Ī·š± ,  url =>"https://telegram.me/Team_SD"]
        ],
        [
        [ text => šSudanese|Gamersš ,  url =>"https://telegram.me/Antar_AlGame"]
        ],
         [
        [ text => Ų¹ŁŲÆŲ© š   ,  callback_data =>"home"]
        ],
]
])
]);
}


if($data=="home"){
   bot( editMessageText ,[
    chat_id =>$chat_id2,
     message_id =>$message_id,
  text =>"Ų§ŁŁŲ§ ŲØŁ Ų¹Ų²ŁŲ²Ł š¹ ŁŁ Ų§ŁŲØŁŲŖ Ų§ŁŲ±Ų³ŁŁ š¶\nŲ§ŁŲ®Ų§Ųµ ŁŲ­ŁŲ§ŁŲ© Ų§ŁŁŲ¬ŁŁŲ¹Ų§ŲŖ š„š\nŁŲ¹ŁŁ ŲØŁ ŁŲŗŲ© Ų§ŁŲ¹Ų±ŲØŁŲ© š ŁŁŲ­ŲŖŁŁ \nŲ¹ŁŁ Ų¬ŁŁŲ¹ Ų§ŁŲ§Ų“ŁŲ§Ų” Ų§ŁŲŖŁ ŲŖŲ­ŲŖŲ§Ų¬ŁŲ§ š\nŁŲ¹ŁŁ ŁŲ¬ŁŁŲ¹Ų© Ų§ŁŁŲ© ŁŲ¬ŁŲÆŲ© ā¼ļø",
 reply_markup =>json_encode([
 inline_keyboard =>[
[
[ text => ŲŖŲ§ŲØŲ¹ Ų¬ŲÆŁŲÆŁŲ§ šŖ ,  callback_data =>"channel2"]
],
[
[ text => Ų§Ų¶ŁŁŁ Ų§ŁŁ ŁŲ¬ŁŁŲ¹ŲŖŁ š¹ā ,  url =>"https://telegram.me/AntarSDbot?startgroup=start"]
],
[
[ text => Ų“Ų§Ų±Ł Ų§ŁŲØŁŲØ š¤š ,  switch_inline_query =>""]
],
[
[ text =>"ŁŁ ŁŲÆŁŁ Ų³Ų¤Ų§Ł ā ","url"=>"https://telegram.me/Team_Sudan"]
]
]
])
]);
}

if($message->reply_to_message && $text == "ŁŲ¹ŁŁŁŲ§ŲŖ"){
bot( sendMessage ,[
 chat_id =>$chat_id,
 text =>"š­Ų§ŁŲ§ŁŲÆŁ : " . $message->reply_to_message->from->id . "\nš­Ų§ŁŁŁŲ²Ų± : @" . $message->reply_to_message->from->username,
 reply_to_message_id =>$message->message_id,
]);
}


if($text == "ŲŗŲ§ŲÆŲ±" && in_array($from_id, $admins)){
bot( kickChatMember ,[
 chat_id =>$chat_id,
 user_id =>$bot_id
]);
}

$bc = explode("/bc", $text);

if($bc && in_array($from_id, $admins)){
$real = file_get_contents("tg/start.txt");
$ex_real = explode("\n", $real);
for($y=0;$y<count($ex_real); $y++){
bot( sendMessage , [
 chat_id  => $ex_real[$y],
 text  => $bc[1]
]);
}
}

$time = time() + (979 * 11 + 1 + 30);
if($text == "Ų§ŁŁŁŲŖ"){
bot( sendMessage ,[
 chat_id =>$chat_id,
 text =>"š Ų§ŁŲØŁŲÆ : Ų§ŁŲ³ŁŲÆŲ§Ł" . "\n" . "š Ų§ŁŲ³Ų§Ų¹Ų© : " . date( g , $time) . "\n" . "š Ų§ŁŲÆŁŁŁŲ© : " . date( i , $time),
 reply_to_message_id =>$message->message_id,
]);
}

if($text == "Ų§ŁŲŖŲ§Ų±ŁŲ®"){
bot( sendMessage ,[
 chat_id =>$chat_id,
 text =>"š Ų§ŁŲØŁŲÆ : Ų§ŁŲ³ŁŲÆŲ§Ł \n" . "š  Ų§ŁŲ³ŁŲ© : " . date("Y") . "\n" . "š Ų§ŁŲ“ŁŲ± : " . date("n") . "\n" . "š Ų§ŁŁŁŁ :" . date("j"),
 reply_to_message_id =>$message->message_id
]);
}

if($text == "ŁŲ³Ų§Ų¹ŲÆŲ©"){
bot( sendMessage ,[
 chat_id =>$chat_id,
 text =>"ŁŁŁŁŲ© Ų§Ų³ŲŖŲ®ŲÆŲ§Ł Ų§ŁŲØŁŲŖ šš»",
 reply_to_message_id =>$message->message_id,
 reply_markup =>json_encode([
 inline_keyboard =>[
[
[ text =>"Ų§ŁŲ§ŁŲ± Ų§ŁŁŁŁ ā", "callback_data"=>"close"]
],
[
["text"=>"Ų§ŁŲ§ŁŲ± Ų§ŁŁŲŖŲ­ ā", "callback_data"=>"open"]
],
[
["text"=>"Ų§ŁŲ§ŁŲ± Ų¹Ų§ŁŲ© š", "callback_data"=>"offc"]
],
[
[ text =>"Ų§ŲµŲÆŲ± Ų§ŁŲØŁŲŖ ŲØŲŖŲ§Ų±ŁŲ® š 2017/5/11 ā", "callback_data"=>"omar"]
]
]
])
]);
}

if($data == "close"){
bot( editMessageText , [
 chat_id =>$chat_id2,
 text =>"Ų§ŁŲ§ŁŲ± Ų§ŁŁŁŁ ŁŁ Ų§ŁŁŲ¬ŁŁŲ¹Ų© š„š",
 message_id =>$message_id,
 reply_markup =>json_encode([
 inline_keyboard =>[
[
[ text =>"Ų§ŁŲ§ŁŲ± Ų§ŁŁŁŁ š", "callback_data"=>"omar"]
],
[
[ text => Ų§ŁŲ±ŁŲ§ŲØŲ· ,  callback_data =>"omar"],
[ text => Ų§ŁŁŁ ,  callback_data =>"omar"]
],
[
[ text => Ų§ŁŲŖŁŲ¬ŁŁ ,  callback_data =>"omar"],
[ text => Ų§ŁŁŁ ,  callback_data =>"omar"]
],
[
[ text => Ų§ŁŁŁŲµŁŲ§ŲŖ ,  callback_data =>"omar"],
[ text => Ų§ŁŁŁ ,  callback_data =>"omar"]
],
[
[ text => Ų§ŁŁŁŲ§ŁŲ“ ,  callback_data =>"omar"],
[ text => Ų§ŁŁŁ ,  callback_data =>"omar"]
],
[
[ text => Ų§ŁŲµŁŲ± ,  callback_data =>"omar"],
[ text => Ų§ŁŁŁ ,  callback_data =>"omar"]
],
[
[ text => Ų§ŁŲµŁŲŖŁŲ§ŲŖ ,  callback_data =>"omar"],
[ text => Ų§ŁŁŁ ,  callback_data =>"omar"]
],
[
[ text => Ų§ŁŲ§ŲŗŲ§ŁŁ ,  callback_data =>"omar"],
[ text => Ų§ŁŁŁ ,  callback_data =>"omar"]
],
[
[ text => Ų¬ŁŲ§ŲŖ Ų§ŁŲ§ŲŖŲµŲ§Ł ,  callback_data =>"omar"],
[ text => Ų§ŁŁŁ ,  callback_data =>"omar"]
],
[
[ text => Ų§ŁŲ§Ų“Ų¹Ų§Ų±Ų§ŲŖ ,  callback_data =>"omar"],
[ text => Ų§ŁŁŁ ,  callback_data =>"omar"]
],
[
[ text => Ų§ŁŲÆŲ±ŲÆŲ“Ų© ,  callback_data =>"omar"],
[ text => Ų§ŁŁŁ ,  callback_data =>"omar"]
],
[
[ text =>"Ų¹ŁŲÆŲ© š ",  callback_data =>"help"]
]
]
])
]);
}

if($data == "open"){
bot( editMessageText , [
 chat_id =>$chat_id2,
 message_id =>$message_id,
 text =>"Ų§ŁŲ§ŁŲ± Ų§ŁŁŲŖŲ­ ŁŁ Ų§ŁŁŲ¬ŁŁŲ¹Ų© š„š",
 reply_markup =>json_encode([
 inline_keyboard =>[
[
[ text =>"Ų§ŁŲ§ŁŲ± Ų§ŁŁŲŖŲ­ š", "callback_data"=>"omar"]
],
[
[ text => Ų§ŁŲ±ŁŲ§ŲØŲ· ,  callback_data =>"omar"],
[ text => Ų§ŁŲŖŲ­ ,  callback_data =>"omar"]
],
[
[ text => Ų§ŁŲŖŁŲ¬ŁŁ ,  callback_data =>"omar"],
[ text => Ų§ŁŲŖŲ­ ,  callback_data =>"omar"]
],
[
[ text => Ų§ŁŁŁŲµŁŲ§ŲŖ ,  callback_data =>"omar"],
[ text => Ų§ŁŲŖŲ­ ,  callback_data =>"omar"]
],
[
[ text => Ų§ŁŁŁŲ§ŁŲ“ ,  callback_data =>"omar"],
[ text => Ų§ŁŲŖŲ­ ,  callback_data =>"omar"]
],
[
[ text => Ų§ŁŲµŁŲ± ,  callback_data =>"omar"],
[ text => Ų§ŁŲŖŲ­ ,  callback_data =>"omar"]
],
[
[ text => Ų§ŁŲµŁŲŖŁŲ§ŲŖ ,  callback_data =>"omar"],
[ text => Ų§ŁŲŖŲ­ ,  callback_data =>"omar"]
],
[
[ text => Ų§ŁŲ§ŲŗŲ§ŁŁ ,  callback_data =>"omar"],
[ text => Ų§ŁŲŖŲ­ ,  callback_data =>"omar"]
],
[
[ text => Ų§ŁŲ§Ų“Ų¹Ų§Ų±Ų§ŲŖ ,  callback_data =>"omar"],
[ text => Ų§ŁŲŖŲ­ ,  callback_data =>"omar"]
],
[
[ text => Ų¬ŁŲ§ŲŖ Ų§ŁŲ§ŲŖŲµŲ§Ł ,  callback_data =>"omar"],
[ text => Ų§ŁŲŖŲ­ ,  callback_data =>"omar"]
],
[
[ text => Ų§ŁŲÆŲ±ŲÆŲ“Ų© ,  callback_data =>"omar"],
[ text => Ų§ŁŲŖŲ­ ,  callback_data =>"omar"]
],
[
[ text =>"Ų¹ŁŲÆŲ© š ",  callback_data =>"help"]
]
]
])
]);
}

if($data == "help"){
bot( editMessageText , [
 chat_id =>$chat_id2,
 message_id =>$message_id,
 text =>"ŁŁŁŁŲ© Ų§Ų³ŲŖŲ®ŲÆŲ§Ł Ų§ŁŲØŁŲŖ šš»",
 reply_markup =>json_encode([
 inline_keyboard =>[
[
[ text =>"Ų§ŁŲ§ŁŲ± Ų§ŁŁŁŁ ā", "callback_data"=>"close"]
],
[
["text"=>"Ų§ŁŲ§ŁŲ± Ų§ŁŁŲŖŲ­ ā", "callback_data"=>"open"]
],
[
["text"=>"Ų§ŁŲ§ŁŲ± Ų¹Ų§ŁŲ© š", "callback_data"=>"offc"]
]
]
])
]);
}

if($data == "offc"){
bot( editMessageText ,[
 chat_id =>$chat_id2,
 message_id =>$message_id,
 text =>"Ų§ŁŲ§ŁŲ§ŁŲ± Ų§ŁŲ¹Ų§ŁŲ© ŁŁ Ų§ŁŁŲ¬ŁŁŲ¹Ų© ā¼ļøš»",
 reply_markup =>json_encode([
 inline_keyboard =>[
[
[ text =>"Ų§ŁŁŲµŁ š»","callback_data"=>"omar" ],
[ text =>"Ų§ŁŲ§ŁŲ± š»","callback_data"=>"omar" ]
],
[
[ text =>"ŁŲ·Ų±ŲÆ Ų§ŁŲ¹Ų¶Ł ŲØŁŲ±ŲÆ","callback_data"=>"omar" ],
[ text =>"Ų·Ų±ŲÆ","callback_data"=>"omar" ]
],
[
[ text =>"ŁŁŲŖŁ Ų¹Ų¶Ł","callback_data"=>"omar" ],
[ text =>"ŁŲŖŁ","callback_data"=>"omar" ]
],
[
[ text =>"ŁŲ§Ų²Ų§ŁŲ© Ų§ŁŁŲŖŁ","callback_data"=>"omar" ],
[ text =>"Ų§ŁŲŗŲ§Ų” Ų§ŁŁŲŖŁ","callback_data"=>"omar" ]
],
[
[ text =>"ŁŁŁŲŗŲ§ŲÆŲ±Ų© ŁŁ Ų§ŁŁŲ¬ŁŁŲ¹Ų©","callback_data"=>"omar" ],
[ text =>"ŁŲŗŲ§ŲÆŲ±Ų©","callback_data"=>"omar" ]
],
[
[ text =>"ŁŲ§Ų¶ŁŲ§Ų± ŁŲ¹ŁŁŁŲ§ŲŖŁ","callback_data"=>"omar" ],
[ text =>"ŁŲ¹ŁŁŁŲ§ŲŖ","callback_data"=>"omar" ]
],
[
[ text =>"ŲØŁŲ±ŲÆ Ų¹ŁŁ Ų¹Ų¶Ł","callback_data"=>"omar" ],
[ text =>"ŁŲ¹ŁŁŁŲ§ŲŖ","callback_data"=>"omar" ]
],
[
[ text =>"ŁŲ§ŁŲŗŲ§Ų” Ų­Ų¶Ų± ŲØŁŲ±ŲÆ","callback_data"=>"omar" ],
[ text => Ų§ŁŲŗŲ§Ų” Ų§ŁŲ­Ų¶Ų± , "callback_data"=>"omar" ]
],
[
[ text =>"ŁŲ¹Ų±Ų¶ Ų§ŁŁŁŲŖ","callback_data"=>"omar"],
[ text =>"Ų§ŁŁŁŲŖ", "callback_data"=>"omar"]
],
[
[ text =>"ŁŲ¹Ų±Ų¶ Ų§ŁŲŖŲ§Ų±ŁŲ®","callback_data"=>"omar"],
[ text =>"Ų§ŁŲŖŲ§Ų±ŁŲ®","callback_data"=>"omar"]
],
[
[ text =>"Ų¹ŲÆŲÆ Ų±Ų³Ų§Ų¦Ł Ų§ŁŁŲ¬ŁŁŲ¹Ų©","callback_data"=>"omar" ],
[ text =>"Ų¹ŲÆŲÆ Ų§ŁŲ±Ų³Ų§Ų¦Ł","callback_data"=>"omar" ]
],
[
[ text =>"Ų¹ŁŲÆŲ© š ",  callback_data =>"help"]
]
]
])
]);
}

if($text == "Ų¹ŲÆŲÆ Ų§ŁŲ±Ų³Ų§Ų¦Ł" && $message->message_id > 1000 && $message->chat->type == "supergroup"){
bot( sendMessage ,[
 chat_id =>$chat_id,
 text =>"Ų¹ŲÆŲÆ š Ų±Ų³Ų§Ų¦Ł Ų§ŁŁŲ¬ŁŁŲ¹Ų© š„š¹  : " . "*$message->message_id*" . "\nŲŖŁŲ§ŁŁŲ§ š” ŁŲ¬ŁŁŲ¹ŲŖŁ ŁŲŖŁŲ§Ų¹ŁŲ© šÆ ",
 reply_to_message_id =>$message->message_id,
 parse_mode => Markdown 
]);   
}

if($text == "Ų¹ŲÆŲÆ Ų§ŁŲ±Ų³Ų§Ų¦Ł" && $message->message_id < 1000 && $message->chat->type == "supergroup"){
bot( sendMessage ,[
 chat_id =>$chat_id,
 text =>"Ų¹ŲÆŲÆ š Ų±Ų³Ų§Ų¦Ł Ų§ŁŁŲ¬ŁŁŲ¹Ų© š„š¹  : " . "*$message->message_id*" . "\nŁŁŲ§Ų³ŁāļøŁŲ¬ŁŁŲ¹ŲŖŁ ŲŗŁŲ± ŁŲŖŁŲ§Ų¹ŁŲ© š¹š­",
 reply_to_message_id =>$message->message_id,
 parse_mode => Markdown 
]);   
}

$ban = explode(" ", $text);
if($ban[0] == "Ų­Ų¶Ų±" && $ban[1] == "Ų¹Ų§Ł" && $ban[2] == $text && in_array($from_id, $admins)){
file_put_contents("tg/banall.txt", "\n" . $ban[2]);

bot( sendMessage ,[
 chat_id =>$chat_id,
 text =>"Ų§ŁŲ¹Ų¶Ł š¹ : " . $ban[2] . "\nŲŖŁ ā Ų­Ų¶Ų±Ł Ų¹Ų§Ł ā¼ļø",
 reply_to_message_id =>$message->message_id,
]);
} 

if($message->reply_to_message && $text == "Ų­Ų¶Ų± Ų¹Ų§Ł" && in_array($from_id, $admins)){
file_put_contents( tg/banall.txt , "\n" . $message->reply_to_message->from->id, FILE_APPEND);
bot( sendMessage ,[
 chat_id =>$chat_id,
 text =>"Ų§ŁŲ¹Ų¶Ł š¹ : @" . $message->reply_to_message->from->username . "\nŲŖŁ ā Ų­Ų¶Ų±Ł Ų¹Ų§Ł ā¼ļø "
]);
}


$get_ban = file_get_contents( tg/banall.txt );
$ex_ban = explode("\n", $get_ban);
if($text && in_array($from_id, $ex_ban)){
bot( sendMessage ,[
 chat_id =>$chat_id,
 text =>"Ų§ŁŲŖ ŁŲ­Ų¶ŁŲ± Ų¹Ų§Ł ŁŁ Ų§ŁŲØŁŲŖ ā¼ļø\nŁŲØŲÆŁ Ų§ŁŁ Ų§Ų³Ų¦ŲŖ Ų§ŁŲ§Ų³ŲŖŲ®ŲÆŲ§Ł š¤ā\nŲŖŁŲØŁŁ ŁŁŲ¬ŁŁŲ¹ Ų³ŁŲŖŁ Ų­Ų¶Ų±Ł š\nŲ§Ų°Ų§ Ų§Ų³Ų£ŲŖ Ų§ŁŲ§Ų³ŲŖŲ®ŲÆŲ§Ł š” ŁŲ±Ų¬Ł ŁŁŁŁ \nŲ¹ŲÆŁ ā Ų§ŁŲ§Ų³Ų§Ų¦Ų© ŲÆŲ§Ų®Ł Ų§ŁŁŲ¬ŁŁŲ¹Ų§ŲŖ Ų§ŁŲŖŁ ŁŲŖŁŲ§Ų¬ŲÆ ŁŁŁŲ§ Ų§ŁŲØŁŲŖ š¤āļø",
 reply_to_message_id =>$message->message_id,
 reply_markup =>json_encode([
 inline_keyboard =>[
[
[ text =>"Ų±Ų§Ų³Ł š¬ Ų§ŁŲÆŲ¹Ł ŁŲ§Ų²Ų§ŁŲ© Ų§ŁŲ­Ų¶Ų± ā¼ļø", "url"=>"https://telegram.me/AntarBoxBot"]
]
]
])
]);
bot( kickChatMember ,[
 chat_id =>$chat_id,
 user_id =>$message->from->id
]);
}

if($message->reply_to_message && $text == "Ų§ŁŲŗŲ§Ų” Ų§ŁŲ¹Ų§Ł" && in_array($from_id, $admins)){
$o = file_get_contents( banall.txt );
$o = str_replace($ban[2],  ,$o);
$o = preg_replace("/(^[\r\n]*|[\r\n]+)[\s\t]*[\r\n]+/", "\n", $o);
file_put_contents( tg/banall.txt , $o);
bot( sendMessage ,[
 chat_id =>$chat_id,
 text =>"Ų§ŁŲ¹Ų¶Ł š¹ : @" . $message->reply_to_message->from->username . "\nŲŖŁ ā Ų§ŁŲŗŲ§Ų” Ų­Ų¶Ų±Ł ŁŁ Ų¹Ų§Ł ā¼ļø "
]);
}

if($ban[0] == "Ų§ŁŲŗŲ§Ų”" && $ban[1] == "Ų§ŁŲ¹Ų§Ł" && $ban[2] == $text && in_array($from_id, $admins)){
$o = file_get_contents( banall.txt );
$o = str_replace($message->reply_to_message->from->id,  ,$o);
$o = preg_replace("/(^[\r\n]*|[\r\n]+)[\s\t]*[\r\n]+/", "\n", $o);
file_put_contents( tg/banall.txt , $o);
bot( sendMessage ,[
 chat_id =>$chat_id,
 text =>"Ų§ŁŲ¹Ų¶Ł š¹ : @" . $message->reply_to_message->from->username . "\nŲŖŁ ā Ų§ŁŲŗŲ§Ų” Ų­Ų¶Ų±Ł ŁŁ Ų¹Ų§Ł ā¼ļø "
]);
}

if($text == "ŁŲŗŲ§ŲÆŲ±Ų©" && strpos($inch ,  "status":"member" ) !== false && $message->chat->type == "supergroup"){
bot( kickChatMember ,[
 chat_id =>$chat_id,
 user_id =>$message->from->id
]);

bot( sendMessage , [
 chat_id =>$chat_id,
 text =>"ŁŲÆŲ§Ų¹Ų§ Ų¹Ų²ŁŲ²Ł āØ",
 reply_to_message_id =>$message->message_id,
]);
}


if($text == "ŁŲŗŲ§ŲÆŲ±Ų©" && strpos($inch ,  "status":"member" ) == false && $message->chat->type == "supergroup"){
bot( sendMessage , [
 chat_id =>$chat_id,
 text => Ų¹Ų°Ų±Ų§ ā¼ļø Ų§ŁŲŖ ŁŲ“Ų±Ł ŁŁ Ų§ŁŁŲ¬ŁŁŲ¹Ų© š¹š ,
 reply_to_message_id =>$message->message_id,
]);
}


if($text && strpos($bot_memb ,  "status":"member" ) !== false && $message->chat->type == "supergroup" && strpos($inch ,  "status":"creator" ) !== false){
bot( sendMessage ,[
 chat_id =>$chat_id,
 text =>"Ų¹Ų°Ų±Ų§ ā¼ļø Ų§ŁŲ§ ŁŲ³ŲŖ ŁŲ“Ų±Ł ŁŁ Ų§ŁŁŲ¬ŁŁŲ¹Ų© ā\nŁŲ§ ŁŁŁŁŁŁ Ų§ŁŲ¹ŁŁ Ų§ŁŲ§Ł š§ Ų§ŁŲ±Ų¬Ų§Ų” ŁŁ ŲØŲŖŲ±ŁŁŲŖŁ ŁŲ“Ų±Ł ŁŁ Ų§ŁŁŲ¬ŁŁŲ¹Ų© š„\nŁŲØŲ¹ŲÆŁŲ§ Ų§Ų±Ų³Ł š§ ŁŲ³Ų§Ų¹ŲÆŲ©",
 reply_markup =>json_encode([
 inline_keyboard =>[
[
[ text => ŲŖŲ§ŲØŲ¹ Ų¬ŲÆŁŲÆŁŲ§ šŖ ,  callback_data =>"channel"]
],
]
])
]);
}

if($text == "ŲŗŲ§ŲÆŲ± Ų§ŁŁŲ¬ŁŁŲ¹Ų©"  && strpos($inch ,  "status":"creator" ) !== false){
bot( kickChatMember ,[
 chat_id =>$chat_id,
 user_id =>$bot_id,
]);
}





if($text == "ŲŗŲ§ŲÆŲ± Ų§ŁŁŲ¬ŁŁŲ¹Ų©"  && strpos($inch ,  "status":"creator" ) == false){
bot( sendMessage ,[
 chat_id =>$chat_id,
 text => Ų¹Ų°Ų±Ų§ ā¼ļø ŁŁŲ· ŁŁŲ“Ų¦ Ų§ŁŁŲ¬ŁŁŲ¹Ų© š„ ŁŁŁŁŁ Ų§Ų³ŲŖŲ®ŲÆŲ§Ł ŁŲ§Ų°Ų§ Ų§ŁŲ§ŁŲ± ā»ļøšŗ ,
 reply_to_message_id =>$message->message_id
]);
}







if($text == "/start" && $message->chat->type == "supergroup"){
bot( sendMessage ,[
 chat_id =>$chat_id,
 text =>"Ų§ŁŁŲ§ ŲØŁ ā Ų§Ų±Ų³Ł ŁŲ³Ų§Ų¹ŲÆŲ© ŁŁŲ¹Ų±ŁŲ© š ŁŁŁŁŲ© Ų§Ų³ŲŖŲ®ŲÆŲ§Ł Ų§ŁŲØŁŲŖ š¤š",
 reply_to_message_id =>$message->message_id
]);
}
