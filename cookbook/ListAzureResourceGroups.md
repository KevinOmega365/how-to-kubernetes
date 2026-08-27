# List Azure Resource Groups

## List all your resource groups as a table

``` terminal
az group list --output table
```

## drop the list into a JSON file

In your current directory

``` terminal
[System.IO.File]::WriteAllText("$pwd\az_group_list.json", (az group list | Out-String))
```
