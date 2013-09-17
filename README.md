XCodeSnippets
=============

##Weak Self

```objective-c
__weak typeof(self)weakSelf = self;
```

##Singleton

```objective-c
+ (instancetype)shared<#name#> {
    static <#class#> *_shared<#name#> = nil;
    static dispatch_once_t onceToken;
    dispatch_once(&onceToken, ^{
        _shared<#name#> = <#initializer#>;
    });
    
    return _shared<#name#>;
}
```

##Log String

```objective-c
NSLog(@"%@", <#string#>);
```

##Log Pretty Function

```objective-c
NSLog(@"%s", __PRETTY_FUNCTION__);
```

##Log Call Stack Symbols

```objective-c
NSLog(@"Call Stack: %@", [NSThread callStackSymbols]);
```


##Dispatch Async

```objective-c
dispatch_async(dispatch_get_global_queue(<#dispatch_queue_priority_t priority#>, <#unsigned long flags#>), ^(void) {
    <#code#>
    
    dispatch_async(dispatch_get_main_queue(), ^(void) {
        <#code#>
    });
});
```

##ARC Dealloc

```objective-c
- (void)dealloc
{
    NSLog(@"%s", __PRETTY_FUNCTION__);
}
```
