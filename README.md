# Gradient CLI

Choose the command that matches your machine.

## macOS / Linux

### macOS (Apple Silicon / arm64)
```bash
curl -fsSL https://github.com/use-gradient/cli/releases/latest/download/gradient-darwin-arm64 -o /tmp/gradient && chmod +x /tmp/gradient && sudo install -m 0755 /tmp/gradient /usr/local/bin/gradient && rm -f /tmp/gradient && gradient --version
```

### macOS (Intel / amd64)
```bash
curl -fsSL https://github.com/use-gradient/cli/releases/latest/download/gradient-darwin-amd64 -o /tmp/gradient && chmod +x /tmp/gradient && sudo install -m 0755 /tmp/gradient /usr/local/bin/gradient && rm -f /tmp/gradient && gradient --version
```

### Linux (arm64)
```bash
curl -fsSL https://github.com/use-gradient/cli/releases/latest/download/gradient-linux-arm64 -o /tmp/gradient && chmod +x /tmp/gradient && sudo install -m 0755 /tmp/gradient /usr/local/bin/gradient && rm -f /tmp/gradient && gradient --version
```

### Linux (amd64)
```bash
curl -fsSL https://github.com/use-gradient/cli/releases/latest/download/gradient-linux-amd64 -o /tmp/gradient && chmod +x /tmp/gradient && sudo install -m 0755 /tmp/gradient /usr/local/bin/gradient && rm -f /tmp/gradient && gradient --version
```

## Windows (PowerShell)

### Windows (arm64)
```powershell
$bin="$HOME\bin"; New-Item -ItemType Directory -Force $bin | Out-Null; Invoke-WebRequest "https://github.com/use-gradient/cli/releases/latest/download/gradient-windows-arm64.exe" -OutFile "$bin\gradient.exe"; $p=[Environment]::GetEnvironmentVariable("Path","User"); if ($p -notlike "*$bin*") { [Environment]::SetEnvironmentVariable("Path", (($p.TrimEnd(';') + ';' + $bin).Trim(';')), "User") }; & "$bin\gradient.exe" --version
```

### Windows (amd64)
```powershell
$bin="$HOME\bin"; New-Item -ItemType Directory -Force $bin | Out-Null; Invoke-WebRequest "https://github.com/use-gradient/cli/releases/latest/download/gradient-windows-amd64.exe" -OutFile "$bin\gradient.exe"; $p=[Environment]::GetEnvironmentVariable("Path","User"); if ($p -notlike "*$bin*") { [Environment]::SetEnvironmentVariable("Path", (($p.TrimEnd(';') + ';' + $bin).Trim(';')), "User") }; & "$bin\gradient.exe" --version
```

Restart your terminal after install if `gradient` is not immediately available on your `PATH`.
