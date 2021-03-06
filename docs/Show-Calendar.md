---
external help file: PSCalendar-help.xml
Module Name: PSCalendar
online version:
schema: 2.0.0
---

# Show-Calendar

## SYNOPSIS

Display a colorized calendar month in the console.

## SYNTAX

```yaml
Show-Calendar [[-Month] <String>] [-Year <Int32>] [-HighlightDate <String[]>] [-HighlightColor <ConsoleColor>]
 [<CommonParameters>]
```

## DESCRIPTION

This command is a wrapper for Get-Calendar that will display the specified month in a colorized format. The command uses Write-Host so it does not write anything to the pipeline.

## EXAMPLES

### EXAMPLE 1

```powershell
PS C:\> Show-Calendar
```

Display a colorized version of the current month. The current day will also be colorized.

### EXAMPLE 2

```powershell
PS C:\> Show-Calendar -Month February -Year 2019 -HighlightDate 2/22/19 -HighlightColor red
```

Display February 2019 and highlight the 22nd in red.

## PARAMETERS

### -Month

Select a month to display. The command will default to the current year unless otherwise specified.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: Current month
Accept pipeline input: False
Accept wildcard characters: False
```

### -Year

Select a year for the specified month.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: current year
Accept pipeline input: False
Accept wildcard characters: False
```

### -HighlightDate

Specific days (named) to highlight. These dates are surrounded by asterisk characters.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-Date).date.toString()
Accept pipeline input: False
Accept wildcard characters: False
```

### -HighlightColor

Specify a console color to use for the highlighted dates.

```yaml
Type: ConsoleColor
Parameter Sets: (All)
Aliases:
Accepted values: Black, DarkBlue, DarkGreen, DarkCyan, DarkRed, DarkMagenta, DarkYellow, Gray, DarkGray, Blue, Green, Cyan, Red, Magenta, Yellow, White

Required: False
Position: Named
Default value: Green
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters

This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.
For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### None

## OUTPUTS

### None

## NOTES

This command should have an alias of scal.

Learn more about PowerShell: http://jdhitsolutions.com/blog/essential-powershell-resources/

## RELATED LINKS

[Get-Calendar]()

[Show-GuiCalendar]()
