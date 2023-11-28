# DevAxCmmRtsLog
Tool for log request and response between, RTS and RetailServer


## Installation

### Using Power Shell
Copy and past
```powershell
# Task 1: Clone the repository
$repositoryUrl = "https://github.com/JonatanTorino/DevAxCmmRtsLog"
$localPath = "K:\Axxon\GitHub.JonatanTorino\DevAxCmmRtsLog"

# Clone the repository
git clone $repositoryUrl $localPath

# Task 2: Create a symbolic link
$targetPath = "K:\Axxon\GitHub.JonatanTorino\DevAxCmmRtsLog"
$linkPath = "K:\AosService\PackagesLocalDirectory\DevAxCmmRtsLog"

# Remove existing directory if it exists
Remove-Item -Path $linkPath -Recurse -Force -ErrorAction SilentlyContinue

# Create a symbolic link
New-Item -ItemType SymbolicLink -Path $linkPath -Target $targetPath

# Set the prompt location to the symbolic link path
Set-Location -Path $linkPath

# Execute the D365 module compile command
Invoke-D365ModuleFullCompile -Module DevAxCmmRtsLog
```