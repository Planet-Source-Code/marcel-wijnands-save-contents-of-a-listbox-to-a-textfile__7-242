<div align="center">

## Save contents of a listbox to a textfile


</div>

### Description

Save contents of a listbox to a textfile
 
### More Info
 
usage:

ListBox2File('c:\yourfile.txt',List1);


<span>             |<span>
---                |---
**Submitted On**   |
**By**             |[Marcel Wijnands](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByAuthor/marcel-wijnands.md)
**Level**          |Beginner
**User Rating**    |5.0 (15 globes from 3 users)
**Compatibility**  |Delphi 5, Delphi 4
**Category**       |[Files/ File Controls/ Input/ Output](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByCategory/files-file-controls-input-output__7-3.md)
**World**          |[Delphi](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByWorld/delphi.md)
**Archive File**   |[](https://github.com/Planet-Source-Code/marcel-wijnands-save-contents-of-a-listbox-to-a-textfile__7-242/archive/master.zip)

### API Declarations

Copyright VB2Delphi.com 2000


### Source Code

```
procedure ListBox2File(sFile: String; oList: TListBox);
var fFile: Text;
var x: Integer;
begin
 AssignFile(fFile,sFile);
 Rewrite(fFile);
 x:=0;
 While x <> oList.Items.Count do
  begin
   writeln(fFile,oList.Items[x]);
   inc(x);
  end;
 CloseFile(fFile);
end;
//visit www.vb2delphi.com for more code!
```

