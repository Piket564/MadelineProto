---
title: destroy_auth_key
description: destroy_auth_key parameters, return type and example
---
## Method: destroy\_auth\_key  
[Back to methods index](index.md)




### Return type: [DestroyAuthKeyRes](../types/DestroyAuthKeyRes.md)

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

$DestroyAuthKeyRes = $MadelineProto->destroy_auth_key();
```

Or, if you're into Lua:

```
DestroyAuthKeyRes = destroy_auth_key({})
```

