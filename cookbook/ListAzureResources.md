# List Azure Resources

## List all your resources as a table

``` terminal
az resource list --output table
```

## drop the list into a JSON file

In your current directory

``` terminal
[System.IO.File]::WriteAllText("$pwd\az_resource_list.json", (az resource list | Out-String))
```
