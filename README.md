$ch = curl_init();
curl_setopt($ch, CURLOPT_URL, "https://api.iplogger.org/ip/info/");
curl_setopt($ch, CURLOPT_HTTPHEADER, [
    'X-token: {api_i6K7rnEQs1PkMDZtvNa0rdyZFv3KPB8s}',
    'Content-Type: multipart/form-data'
]);
curl_setopt($ch, CURLOPT_POST, 1);
curl_setopt($ch, CURLOPT_POSTFIELDS, [
     'ip' => '187.250.219.226'
]);

$res = curl_exec($ch);
curl_close($ch);

$res = json_decode($res, true);

print_r($res);
