---
title: test.callBytes
description: test.callBytes parameters, return type and example
---
## Method: test.callBytes  
[Back to methods index](index.md)


YOU CANNOT USE THIS METHOD IN MADELINEPROTO


### Parameters:

| Name     |    Type       | Required |
|----------|:-------------:|---------:|
|x|[bytes](../types/bytes.md) | Yes|


### Return type: [test\_Bytes](../types/test_Bytes.md)

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

$test_Bytes = $MadelineProto->test->callBytes(['x' => bytes, ]);
```

Or, if you're into Lua:

```
test_Bytes = test.callBytes({x=bytes, })
```

