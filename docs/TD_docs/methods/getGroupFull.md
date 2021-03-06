---
title: getGroupFull
description: Returns full information about a group by its identifier
---
## Method: getGroupFull  
[Back to methods index](index.md)


YOU CANNOT USE THIS METHOD IN MADELINEPROTO


Returns full information about a group by its identifier

### Params:

| Name     |    Type       | Required | Description |
|----------|:-------------:|:--------:|------------:|
|group\_id|[int](../types/int.md) | Yes|Group identifier|


### Return type: [GroupFull](../types/GroupFull.md)

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

$GroupFull = $MadelineProto->getGroupFull(['group_id' => int, ]);
```

Or, if you're into Lua:

```
GroupFull = getGroupFull({group_id=int, })
```

