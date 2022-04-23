# Multi-language Didn't Work in Xcode
## Issue
Run the sample project. The development language was English.
After translated to Chinese and imported back, the app could only run in Chinese.

Workaround:
I can manually added ".strings" files in Xcode by Choosing "English" in File Inspector on the right of Xcode on each Chinese ".strings" files. Then If I commented or removed all items in it. English worked again.

I thought Xcode forgot to create English "strings" files when working with multi-languages. That was the reason why this issue happened. The file could be empty, but it must exist, or the multi-language didn't work.
****
## Steps
1. Create a new project in SwiftUI.
2. Add Chinese translations.
3. Export the translation file, translate and import back.
4. Run the file in both Chinese and English.

### Expected
The app would work in multi-language.

### Happened
The app only worked in Chinese. In English, it still showed in Chinese.