---
title: unblockUser
description: Removes user from black list
---
## Method: unblockUser  
[Back to methods index](index.md)


YOU CANNOT USE THIS METHOD IN MADELINEPROTO


Removes user from black list

### Params:

| Name     |    Type       | Required | Description |
|----------|:-------------:|:--------:|------------:|
|user\_id|[int](../types/int.md) | Yes|User identifier|


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

$Ok = $MadelineProto->unblockUser(['user_id' => int, ]);
```

Or, if you're into Lua:

```
Ok = unblockUser({user_id=int, })
```

