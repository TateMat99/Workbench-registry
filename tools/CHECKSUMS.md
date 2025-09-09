# Compute SHA-256 for a wheel

## macOS / Linux
shasum -a 256 path/to/your.whl

## Windows (PowerShell)
Get-FileHash -Algorithm SHA256 path\to\your.whl
