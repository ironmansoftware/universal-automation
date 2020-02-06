# 0.0.3-beta7 - 1/6/2020

## Added 

- Added -RepositoryPath to Start-UAServer so you can specify where the local Git repo is stored. 
- Added support for authentication on the Swagger page

## Changed

- UA will now work in the ISE
- Stop-UAServer now performs a graceful shutdown by default. Using the -Force parameter forces the process to terminate.
- Fixed an issue where an dashboard without authentication enabled would be in read-only mode

# 0.0.3-beta6 - 1-31-2020

## Added 

- Added Enable-UAAuthentication to make it easier to enable UA authentication. 

## Changed

- Fixed an issue where restarting the server would fail to return a system app token and you could no longer use the UA dashboard (401 error)
- Fixed an issue where scripts' tags would not be sync'd to git - https://github.com/ironmansoftware/universal-automation/issues/67
- Fixed issue with roles not being assigned
- Fixed issue with session AppToken not being used in the dashboard

# 0.0.3-beta5 - 1-22-2020

## Added

- Added UI controls for disabling manual invocation of scripts
- Tags are now stored in the git repo under `.ua/tags.psd1`

## Changed

- Fixed issue where a $null on the pipeline would cause a script to file - https://github.com/ironmansoftware/universal-automation/issues/74
- Fixed an issue where you couldn't cancel a script requesting feedback - https://github.com/ironmansoftware/universal-automation/issues/78
- No trial license required - https://ironmansoftware.com/simplifying-product-trial-licensing/

# 0.0.3-beta4 - 1-18-2020

## Added 

- Added built-in varaibles for $UAScript, $UAJob, and $UASchedule. https://github.com/ironmansoftware/universal-automation/issues/64
- Added -DisableManualInvocation to New-UAScript to prevent jobs from running ad-hoc - https://github.com/ironmansoftware/universal-automation/issues/59

## Changed

- Error output now lists the script stack trace. 
- Fixed an issue with not being able to save PowerShell Version settings - https://github.com/ironmansoftware/universal-automation/issues/71
- Fixed sorting of job tables (clicking now sorts correctly) 
- Fixed issue where schedules would be lost when editing the script content in the dashboard - https://github.com/ironmansoftware/universal-automation/issues/66

# 0.0.3-beta3 - 1-15-2020

## Changed

- Get-UAJob now supports paging, server-side filtering and sorting 
- UA dashboard active and historical job grids now use server-side processing
- Fixing an issue where an AppToken would be generated when executing a script even when AppTokens aren't being used. 
- Fixed issue where license activation would run every time the server was started 
- Fixed issue with dot sourcing files (https://github.com/ironmansoftware/universal-automation/issues/73)
- Fixed sorting of the ID column in the job grid (https://github.com/ironmansoftware/universal-automation/issues/46)

# 0.0.3-beta2 - 1-14-2020

## Changed

- Removed the diagrams component from UniversalAutomation.Dashboard so unlicensed UD dashboards will work. 
