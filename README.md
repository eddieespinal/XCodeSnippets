XCodeSnippets
=============

<b>Weak Self</b>
__weak typeof(self)weakSelf = self;

<b>Singleton</b>

+ (instancetype)shared<#name#> {
    static <#class#> *_shared<#name#> = nil;
    static dispatch_once_t onceToken;
    dispatch_once(&onceToken, ^{
        _shared<#name#> = <#initializer#>;
    });
    
    return _shared<#name#>;
}

