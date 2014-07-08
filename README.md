mobile development notes 
========================



* pod - like bundler dependency manager
* NSLogger - logging framework with a client 
* colorschemerstudio - tools to pick colors 
* Linguan - Tool to manage multilanguages application
* UIKitUICatalog - UI Kit Catalogues
* MobileHIG - Guidelines to write applications
* http://alcatraz.io/
* http://sparkinspector.com/
* moarfonts

# Useful Links 
* http://iosdevtips.co/post/82232620790/best-xcode-plugins


## NSLogger
```
- (BOOL)application:(UIApplication *)application didFinishLaunchingWithOptions:(NSDictionary *)launchOptions
{
    // Customize UI
    [self customizeGlobalAppearance];
    
    // Init CocoaLumberjack NSLogger connector
    [DDLog addLogger:[DDNSLoggerLogger sharedInstance]];
    // Standard lumberjack initialization
    [DDLog addLogger:[DDTTYLogger sharedInstance]];
    // And then enable colors
    [[DDTTYLogger sharedInstance] setColorsEnabled:YES];
    
    return YES;
}
```
