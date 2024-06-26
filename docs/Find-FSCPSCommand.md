﻿---
external help file: fscps.tools-help.xml
Module Name: fscps.tools
online version:
schema: 2.0.0
---

# Find-FSCPSCommand

## SYNOPSIS
Finds fscps.tools commands searching through the inline help text

## SYNTAX

```
Find-FSCPSCommand [[-Pattern] <String>] [[-Tag] <String[]>] [[-Author] <String>] [[-MinimumVersion] <String>]
 [[-MaximumVersion] <String>] [-Rebuild] [-EnableException] [-ProgressAction <ActionPreference>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
Finds fscps.tools commands searching through the inline help text, building a consolidated json index and querying it because Get-Help is too slow

## EXAMPLES

### EXAMPLE 1
```
Find-FSCPSCommand "snapshot"
```

For lazy typers: finds all commands searching the entire help for "snapshot"

### EXAMPLE 2
```
Find-FSCPSCommand -Pattern "snapshot"
```

For rigorous typers: finds all commands searching the entire help for "snapshot"

### EXAMPLE 3
```
Find-FSCPSCommand -Tag copy
```

Finds all commands tagged with "copy"

### EXAMPLE 4
```
Find-FSCPSCommand -Tag copy,user
```

Finds all commands tagged with BOTH "copy" and "user"

### EXAMPLE 5
```
Find-FSCPSCommand -Author Mötz
```

Finds every command whose author contains "Mötz"

### EXAMPLE 6
```
Find-FSCPSCommand -Author Mötz -Tag copy
```

Finds every command whose author contains "Mötz" and it tagged as "copy"

### EXAMPLE 7
```
Find-FSCPSCommand -Rebuild
```

Finds all commands and rebuilding the index (good for developers)

## PARAMETERS

### -Pattern
Searches help for all commands in fscps.tools for the specified pattern and displays all results

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Tag
Finds all commands tagged with this auto-populated tag

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Author
Finds all commands tagged with this author

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MinimumVersion
Finds all commands tagged with this auto-populated minimum version

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MaximumVersion
Finds all commands tagged with this auto-populated maximum version

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Rebuild
Rebuilds the index

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -EnableException
By default, when something goes wrong we try to catch it, interpret it and give you a friendly warning message.
This avoids overwhelming you with "sea of red" exceptions, but is inconvenient because it basically disables advanced scripting.
Using this switch turns this "nice by default" feature off and enables you to catch exceptions with your own try/catch.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: Silent

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Displays what would happen if the command is run

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Confirm
Confirms overwrite of index

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ProgressAction
{{ Fill ProgressAction Description }}

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: proga

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES
Tags: Find, Help, Command
This is refactored function from d365fo.tools

Original Author: Mötz Jensen (@Splaxi)
Author: Oleksandr Nikolaiev (@onikolaiev)

License: MIT https://opensource.org/licenses/MIT

This cmdlet / function is copy & paste implementation based on the Find-DbaCommand from the dbatools.io project

Original author: Simone Bizzotto (@niphold)

## RELATED LINKS
