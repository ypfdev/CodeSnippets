# CodeSnippets - Xcode代码块

### 究竟是什么？

CodeSnippets实质上是后缀为`.codesnippet`类型的文件，内容类似于plist，存放了代码块的各种信息，例如：

```
<?xml version="1.0" encoding="UTF-8"?>
<!DOCTYPE plist PUBLIC "-//Apple//DTD PLIST 1.0//EN" "http://www.apple.com/DTDs/PropertyList-1.0.dtd">
<plist version="1.0">
<dict>
	<key>IDECodeSnippetCompletionPrefix</key>
	<string>x-popToVC</string>
	<key>IDECodeSnippetCompletionScopes</key>
	<array>
		<string>All</string>
	</array>
	<key>IDECodeSnippetContents</key>
	<string>dispatch_async(dispatch_get_main_queue(), ^{
    // pop到栈中指定的控制器
    for (UIViewController *vc in self.navigationController.viewControllers) {
        if ([vc isKindOfClass:&lt;#NSClassFromString(@"MCHomeVC")#&gt;]) {
            [self.navigationController popToViewController:vc animated:YES];
        }
    }
});</string>
	<key>IDECodeSnippetIdentifier</key>
	<string>64D9EF02-2D9B-47EF-B77E-3B8C99C0583F</string>
	<key>IDECodeSnippetLanguage</key>
	<string>Xcode.SourceCodeLanguage.Objective-C</string>
	<key>IDECodeSnippetSummary</key>
	<string>pop到栈中指定的控制器</string>
	<key>IDECodeSnippetTitle</key>
	<string>x-popToVC</string>
	<key>IDECodeSnippetUserSnippet</key>
	<true/>
	<key>IDECodeSnippetVersion</key>
	<integer>2</integer>
</dict>
</plist>

```

### 保存在哪里？

CodeSnippets保存在下面路径中，一旦卸载重装Xcode，这里的文件就会丢失，所以记得做好备份~

```
/Users/ypf/Library/Developer/Xcode/UserData/CodeSnippets
```
