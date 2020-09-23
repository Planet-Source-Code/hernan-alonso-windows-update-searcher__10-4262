<div align="center">

## Windows Update Searcher


</div>

### Description

Search all Microsoft Update Missing
 
### More Info
 
Tittles of Microsoft Updates


<span>             |<span>
---                |---
**Submitted On**   |
**By**             |[Hernan Alonso](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByAuthor/hernan-alonso.md)
**Level**          |Advanced
**User Rating**    |5.0 (10 globes from 2 users)
**Compatibility**  |VB\.NET
**Category**       |[Miscellaneous](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByCategory/miscellaneous__10-1.md)
**World**          |[\.Net \(C\#, VB\.net\)](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByWorld/net-c-vb-net.md)
**Archive File**   |[](https://github.com/Planet-Source-Code/hernan-alonso-windows-update-searcher__10-4262/archive/master.zip)





### Source Code

```
'Refer the COM: WUAPI 2.0 Type Library
Imports WUApiLib.UpdateOperation
Imports WUApiLib.UpdateSessionClass
  Public Sub Get_Updates()
    'Object for seach
    Dim updateSearcher As New WUApiLib.UpdateSearcher
    Dim updateSession As New WUApiLib.UpdateSessionClass
    'Condition
    updateSearcher.Search("IsInstalled=0 and Type='Software'")
    Dim searchResult As WUApiLib.ISearchResult
    Dim Update As WUApiLib.IUpdate
    'Search
    searchResult = updateSearcher.Search("IsInstalled=0")
    'Show Tittles updates
    Dim i As Integer = 0
    For i = 0 To searchResult.Updates.Count - 1
      Update = searchResult.Updates.Item(i)
      MsgBox(Update.Title.ToString)
    Next
  End Sub
```

