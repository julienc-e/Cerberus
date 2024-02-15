#!/usr/bin/env pwsh

Connect-MicrosoftTeams

$TeamID = ""

foreach($studentmail in Get-Content $args[0]) {
        Try {
            Add-TeamUser -GroupId $TeamID -User $studentmail -Role "Member"
            Write-host "Added User:"$studentmail -f Green
        }
        Catch {
            Write-host -f Red "Error Adding User to the Team:" $_.Exception.Message
        }
}
