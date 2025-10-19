# How To Get Data From A `.ndjson` File

New line delimited json files use the extension `.ndjson`.
The file structure is made up of a separate json objects on each new line.
To import this data to a variable requires an extra step.

```powershell
$data = Get-Content -Path "path\to\file.ndjson" | ForEach-Object {$_ | ConvertFrom-Json}
```

There may be a nested structure to the parsed data.
