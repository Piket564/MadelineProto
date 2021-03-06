---
title: downloadFile
description: Asynchronously downloads file from cloud. Updates updateFileProgress will notify about download progress. Update updateFile will notify about successful download
---
## Method: downloadFile  
[Back to methods index](index.md)


YOU CANNOT USE THIS METHOD IN MADELINEPROTO


Asynchronously downloads file from cloud. Updates updateFileProgress will notify about download progress. Update updateFile will notify about successful download

### Params:

| Name     |    Type       | Required | Description |
|----------|:-------------:|:--------:|------------:|
|file\_id|[int](../types/int.md) | Yes|Identifier of file to download|


### Return type: [Ok](../types/Ok.md)

### Example:


```
$MadelineProto = new \danog\MadelineProto\API();
if (isset($token)) { // Login as a bot
    $this->bot_login($token);
}
if (isset($number)) { // Login as a user
    $sentCode = $MadelineProto->phone_login($number);
    echo 'Enter the code you received: ';
    $code = '';
    for ($x = 0; $x < $sentCode['type']['length']; $x++) {
        $code .= fgetc(STDIN);
    }
    $MadelineProto->complete_phone_login($code);
}

$Ok = $MadelineProto->downloadFile(['file_id' => int, ]);
```

Or, if you're into Lua:

```
Ok = downloadFile({file_id=int, })
```

