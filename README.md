<div align="center">

## Currency to text Conversion


</div>

### Description

Converts the Currency to Text. For Ex: 100.90 is converted as one hundred dollars and ninety cents only.
 
### More Info
 
Insert a formula field in crystal reports and Paste the Code and replace the

currencyfield in the code with any reportfield whose datatype is currency or

Integer.

String


<span>             |<span>
---                |---
**Submitted On**   |
**By**             |[Dasari\. Ravi Kumar\(r&d teamworks\)](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByAuthor/dasari-ravi-kumar-r-d-teamworks.md)
**Level**          |Unknown
**User Rating**    |4.3 (65 globes from 15 users)
**Compatibility**  |VB 4\.0 \(16\-bit\), VB 4\.0 \(32\-bit\), VB 5\.0, VB 6\.0
**Category**       |[Miscellaneous](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByCategory/miscellaneous__1-1.md)
**World**          |[Visual Basic](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByWorld/visual-basic.md)
**Archive File**   |[](https://github.com/Planet-Source-Code/dasari-ravi-kumar-r-d-teamworks-currency-to-text-conversion__1-4804/archive/master.zip)





### Source Code

```
if right(totext({currencyfield}),2) = '00' then
uppercase(left(towords(truncate({currencyfield}),0)+' ' +'dollars'+' '+ 'only',1)) + right(towords(truncate({currencyfield}),0)+' ' +'dollars' + ' ' + 'only',length(towords(truncate({currencyfield}),0)+' ' + 'dollars' +' '+ 'only') -1)
else
towords(truncate({currencyfield}),0) +' '+'dollars'+' '+ 'and'+' ' +towords(tonumber(right(TOTEXT({currencyfield}),2)),0)+' '+'cents'+ ' ' + 'only'
```

