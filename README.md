XCodeSnippets
=============

##Weak Self
> csWeakSelf

```objective-c
__weak typeof(self)weakSelf = self;
```

##Singleton
> csSingleton

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
> csLogString

```objective-c
NSLog(@"%@", <#string#>);
```

##Log Pretty Function
> csLogFunction

```objective-c
NSLog(@"%s", __PRETTY_FUNCTION__);
```

##Log Call Stack Symbols
> csLogCallStackSymbols

```objective-c
NSLog(@"Call Stack: %@", [NSThread callStackSymbols]);
```


##Dispatch Async
> csDispatchAsync

```objective-c
dispatch_async(dispatch_get_global_queue(<#dispatch_queue_priority_t priority#>, <#unsigned long flags#>), ^(void) {
    <#code#>
    
    dispatch_async(dispatch_get_main_queue(), ^(void) {
        <#code#>
    });
});
```

##ARC Dealloc
> csDealloc

```objective-c
- (void)dealloc
{
    NSLog(@"%s", __PRETTY_FUNCTION__);
}
```

##NSNotifications Remove Observer
> csRemoveObserver

```objective-c
[[NSNotificationCenter defaultCenter] removeObserver:self
                                                    name:<#notification name#>;
                                                  object:nil];
```