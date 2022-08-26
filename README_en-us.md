# Virtual-Box
##### English | [简体中文](README.md)
## minecraft BE BDS plug-in - player multi backpack system - virtual box
- **This is a BDS plug-in under development**
- Equivalent to player multi backpack expansion
- You can open a virtual backpack in the form of a large box. You can move freely between the virtual box and your own backpack and take out items
### The planned functions include:
- Support the expansion of virtual backpacks (cost), and support page turning;
- Support simple custom virtual backpack expansion cost calculation formula;
- Support OP management to check other people's virtual backpacks;
- Support sharing virtual backpacks with other players;
- Open virbox with the specified item
### Possible features:
- Automatic sorting and sorting of virtual backpacks;
- Item consolidation


### Demo version🎁
 The demo version means that it is not a formal version, and the function is not perfect and experimental. This page is in the demo version test state before the formal completion.
![virboxDEMO版本操作界面](https://user-images.githubusercontent.com/51207072/185733431-2ed6d0a6-cb8c-44fa-bf74-faa3ca226791.png)
### How to install and start
- This plug-in depends on the liteloader BDS launcher (above 2.5.1). After downloading the plug-in, please put the DLL plug-in into the plugins directory and run normally. After entering the game, use the command /virbox to start the operation.
### Brief description of demo version
- Demo version realizes simple operation of taking out, putting in and moving items, and realizes page turning and user-defined virtual backpack expansion cost calculation formula (four operations)
- OP can manage other people's virtual backpacks, /virbox playername
 <br/>But there are some details that need attention:<br>
- First of all, item exchange is not allowed. When items are thrown out, the merging operation is not allowed. Under windows, the merging operation of virtual virbox will directly become "exchanging items selected by the mouse";
- Many original operations in the game have not yet been implemented, and you may receive a warning from the plug-in; If the plug-in pops up an error (not from liteloader), don't worry too much. It is usually handled automatically. If you think it is an error, **Please submit the error description and the recurrence steps in the issue.** 

### configuration file📋
```javascript
{
    "maxpage": 3,//Maximum number of pages that can be unlocked by a player
    "moneymode": 1,//Economic operation mode，1=llmoney，0=scoreboard
    "pagecost": 0,//Page cost is a custom variable, not the final cost.
    "paycalculationformula": "{pagecost}+{page}*{page}*2000",//Unlock the calculation formula that costs money on the next page. It supports four operations. If the formula is wrong, it will cause exceptions or even collapse
    /*Example of formula
    If the configuration item pagecost = 0 and the number of unlocked pages of the current player is page = 1,
Then you need money to unlock the next page: 0 + 1 * 1 * 2000 = 2000
    */
    "scoremoneyname": "money" //Scoreboard name of the scoreboard project for economic docking
}
```
### About the Release Version

- The release of the Release Version is pending. In autumn, the author has many things to do.
- However, if the stars exceeds 50, we should continue to complete this part of the work as soon as possible.



