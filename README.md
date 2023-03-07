# HxDiff

Example usage:

```haxe
final a = new diff.FileData(Bytes.ofString(expected), "expected", Date.now());
final b = new diff.FileData(Bytes.ofString(content), "actual", Date.now());
var ctx:diff.Context = {
  file1: a,
  file2: b,
  context: 10
}

final script = diff.Analyze.diff2Files(ctx);
var diff = diff.Printer.printUnidiff(ctx, script);
Sys.println(diff);
```
