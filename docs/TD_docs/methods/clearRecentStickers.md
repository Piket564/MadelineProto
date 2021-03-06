---
title: clearRecentStickers
description: Clears list of recently used stickers
---
## Method: clearRecentStickers  
[Back to methods index](index.md)


YOU CANNOT USE THIS METHOD IN MADELINEPROTO


Clears list of recently used stickers

### Params:

| Name     |    Type       | Required | Description |
|----------|:-------------:|:--------:|------------:|
|is\_attached|[Bool](../types/Bool.md) | Yes|Pass true to clear list of stickers recently attached to photo or video files, pass false to clear the list of recently sent stickers|


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

$Ok = $MadelineProto->clearRecentStickers(['is_attached' => Bool, ]);
```

Or, if you're into Lua:

```
Ok = clearRecentStickers({is_attached=Bool, })
```

