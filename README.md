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


