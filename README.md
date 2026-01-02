# 🎨 Color

A powerful and elegant Go package for colorful terminal output. Add vibrant colors, text styles, and formatting to your CLI applications with ease.

![Go Version](https://img.shields.io/badge/Go-1.18+-00ADD8?style=flat&logo=go)
![License](https://img.shields.io/badge/License-MIT-green)

## ✨ Features

- 🌈 **16 Standard Colors** - 8 basic + 8 high-intensity foreground colors
- 🖼️ **Background Colors** - Full background color support
- 🎯 **24-bit True Color (RGB)** - Millions of colors at your fingertips
- ✍️ **Text Styles** - Bold, Italic, Underline, Strikethrough, and more
- 🔧 **Flexible API** - Multiple ways to apply colors
- 🖥️ **Cross-Platform** - Works on Windows, macOS, and Linux
- 🚫 **NO_COLOR Support** - Respects the [NO_COLOR](https://no-color.org/) standard

## 📦 Installation

```bash
go get github.com/yourusername/color
```

## 🚀 Quick Start

```go
package main

import "github.com/yourusername/color"

func main() {
    // Simple color printing
    color.Red("This is red text!")
    color.Green("Success! Everything is working.")
    color.Yellow("Warning: Check your configuration.")
    color.Blue("Info: Processing complete.")
    color.Magenta("Debug: Variable value = 42")
    color.Cyan("Note: Remember to commit your changes.")
    
    // High-intensity colors
    color.HiRed("Bright red alert!")
    color.HiGreen("Bright green success!")
    color.HiYellow("Bright yellow warning!")
    color.HiBlue("Bright blue info!")
    color.HiMagenta("Bright magenta debug!")
    color.HiCyan("Bright cyan note!")
}
```

## 🎨 Color Palette

### Foreground Colors

| Standard | High-Intensity |
|----------|----------------|
| `FgBlack` | `FgHiBlack` |
| `FgRed` | `FgHiRed` |
| `FgGreen` | `FgHiGreen` |
| `FgYellow` | `FgHiYellow` |
| `FgBlue` | `FgHiBlue` |
| `FgMagenta` | `FgHiMagenta` |
| `FgCyan` | `FgHiCyan` |
| `FgWhite` | `FgHiWhite` |

### Background Colors

| Standard | High-Intensity |
|----------|----------------|
| `BgBlack` | `BgHiBlack` |
| `BgRed` | `BgHiRed` |
| `BgGreen` | `BgHiGreen` |
| `BgYellow` | `BgHiYellow` |
| `BgBlue` | `BgHiBlue` |
| `BgMagenta` | `BgHiMagenta` |
| `BgCyan` | `BgHiCyan` |
| `BgWhite` | `BgHiWhite` |

### Text Attributes

| Attribute | Description |
|-----------|-------------|
| `Bold` | **Bold text** |
| `Faint` | Dimmed text |
| `Italic` | *Italic text* |
| `Underline` | Underlined text |
| `BlinkSlow` | Slow blinking |
| `BlinkRapid` | Rapid blinking |
| `ReverseVideo` | Swapped foreground/background |
| `Concealed` | Hidden text |
| `CrossedOut` | ~~Strikethrough~~ |

## 📖 Usage Examples

### Creating Custom Colors

```go
// Create a color with multiple attributes
warning := color.New(color.FgYellow, color.Bold)
warning.Println("This is a bold yellow warning!")

// Chain attributes
fancy := color.New(color.FgCyan).Add(color.Underline).Add(color.Bold)
fancy.Println("Fancy cyan, bold, and underlined!")

// Background + Foreground
alert := color.New(color.FgWhite, color.BgRed, color.Bold)
alert.Println(" ALERT: Critical error detected! ")
```

### 24-bit RGB Colors

```go
// Create custom RGB foreground color
coral := color.RGB(255, 127, 80)
coral.Println("Beautiful coral color!")

// Create custom RGB background color
ocean := color.New(color.FgWhite).AddBgRGB(0, 105, 148)
ocean.Println(" Ocean blue background ")

// Gradient-like effect
for i := 0; i < 10; i++ {
    c := color.RGB(255, i*25, 0)
    c.Print("█")
}
fmt.Println()
```

### String Functions (No Printing)

```go
// Get colored strings without printing
redText := color.RedString("Error: %s", "file not found")
greenText := color.GreenString("Success!")
yellowText := color.YellowString("Warning: %d issues", 5)

fmt.Println(redText, greenText, yellowText)

// Hi-intensity string variants
brightRed := color.HiRedString("Bright red!")
brightGreen := color.HiGreenString("Bright green!")
```

### Reusable Color Functions

```go
// Create reusable print functions
info := color.New(color.FgCyan, color.Bold).PrintFunc()
success := color.New(color.FgGreen).PrintlnFunc()
errorPrint := color.New(color.FgRed, color.Bold).PrintfFunc()

info("Processing... ")
success("Done!")
errorPrint("Failed with code: %d\n", 1)

// Create reusable string functions
highlight := color.New(color.FgYellow, color.Bold).SprintFunc()
fmt.Printf("Important: %s\n", highlight("Read this!"))
```

### Mixing Colors in Output

```go
// Mix multiple colors in a single line
red := color.New(color.FgRed).SprintFunc()
green := color.New(color.FgGreen).SprintFunc()
blue := color.New(color.FgBlue).SprintFunc()

fmt.Printf("Status: %s | %s | %s\n", 
    red("Error"), 
    green("Success"), 
    blue("Info"))
```

### Writing to Custom Writers

```go
// Write to stderr with colors
errColor := color.New(color.FgRed, color.Bold)
errColor.Fprintln(color.Error, "This goes to stderr in red!")

// Write to any io.Writer
var buf bytes.Buffer
color.New(color.FgGreen).Fprint(&buf, "Buffered green text")
```

### Temporarily Setting Colors

```go
// Set color for subsequent output
color.Set(color.FgMagenta, color.Bold)
fmt.Println("This is magenta and bold")
fmt.Println("This is also magenta and bold")
color.Unset() // Reset to default
fmt.Println("Back to normal")
```

## 🎭 Practical Examples

### Colorful Log Levels

```go
func logInfo(msg string)    { color.Cyan("ℹ INFO: %s", msg) }
func logSuccess(msg string) { color.Green("✓ SUCCESS: %s", msg) }
func logWarning(msg string) { color.Yellow("⚠ WARNING: %s", msg) }
func logError(msg string)   { color.Red("✗ ERROR: %s", msg) }
func logDebug(msg string)   { color.Magenta("🔍 DEBUG: %s", msg) }

// Usage
logInfo("Application started")
logSuccess("Database connected")
logWarning("Cache is almost full")
logError("Failed to load config")
logDebug("Variable x = 42")
```

### Progress Bar

```go
func printProgress(percent int) {
    filled := percent / 5
    empty := 20 - filled
    
    bar := color.New(color.FgGreen).Sprint(strings.Repeat("█", filled))
    bar += color.New(color.FgWhite).Sprint(strings.Repeat("░", empty))
    
    fmt.Printf("\r[%s] %3d%%", bar, percent)
}
```

### Styled Headers

```go
func printHeader(title string) {
    header := color.New(color.FgHiWhite, color.BgBlue, color.Bold)
    padding := strings.Repeat(" ", 3)
    header.Printf("%s%s%s\n", padding, title, padding)
}

func printSubHeader(title string) {
    sub := color.New(color.FgCyan, color.Underline)
    sub.Println(title)
}
```

### Status Table

```go
type Status int
const (
    StatusOK Status = iota
    StatusWarning
    StatusError
)

func printStatus(name string, status Status) {
    statusColors := map[Status]*color.Color{
        StatusOK:      color.New(color.FgGreen),
        StatusWarning: color.New(color.FgYellow),
        StatusError:   color.New(color.FgRed),
    }
    
    statusText := map[Status]string{
        StatusOK:      "✓ OK",
        StatusWarning: "⚠ WARN",
        StatusError:   "✗ FAIL",
    }
    
    c := statusColors[status]
    fmt.Printf("%-20s %s\n", name, c.Sprint(statusText[status]))
}
```

## ⚙️ Configuration

### Disabling Colors

```go
// Disable globally
color.NoColor = true

// Disable for specific color instance
c := color.New(color.FgRed)
c.DisableColor()

// Re-enable
c.EnableColor()
```

### Environment Variables

Colors are automatically disabled when:

- `NO_COLOR` environment variable is set (any value)
- `TERM=dumb` is set
- Output is not a terminal (e.g., piped to a file)

```bash
# Disable colors via environment
NO_COLOR=1 ./myprogram

# Force dumb terminal
TERM=dumb ./myprogram
```

## 🌈 Color Showcase

```go
package main

import "github.com/yourusername/color"

func main() {
    // Rainbow effect
    colors := []color.Attribute{
        color.FgRed,
        color.FgYellow,
        color.FgGreen,
        color.FgCyan,
        color.FgBlue,
        color.FgMagenta,
    }
    
    text := "RAINBOW"
    for i, char := range text {
        c := color.New(colors[i%len(colors)], color.Bold)
        c.Print(string(char))
    }
    fmt.Println()
    
    // Gradient boxes
    for r := 0; r < 255; r += 25 {
        color.RGB(r, 100, 255-r).Print("█")
    }
    fmt.Println()
    
    // All foreground colors
    fmt.Println("\nForeground Colors:")
    color.Black("  Black  ")
    color.Red("  Red  ")
    color.Green("  Green  ")
    color.Yellow("  Yellow  ")
    color.Blue("  Blue  ")
    color.Magenta("  Magenta  ")
    color.Cyan("  Cyan  ")
    color.White("  White  ")
    
    fmt.Println("\nHi-Intensity Colors:")
    color.HiBlack("  HiBlack  ")
    color.HiRed("  HiRed  ")
    color.HiGreen("  HiGreen  ")
    color.HiYellow("  HiYellow  ")
    color.HiBlue("  HiBlue  ")
    color.HiMagenta("  HiMagenta  ")
    color.HiCyan("  HiCyan  ")
    color.HiWhite("  HiWhite  ")
}
```

## 📚 API Reference

### Package Functions

| Function | Description |
|----------|-------------|
| `New(attrs...)` | Create a new Color with attributes |
| `RGB(r, g, b)` | Create foreground RGB color |
| `BgRGB(r, g, b)` | Create background RGB color |
| `Set(attrs...)` | Set colors for subsequent output |
| `Unset()` | Reset to default colors |

### Color Methods

| Method | Description |
|--------|-------------|
| `Print(a...)` | Print with color |
| `Printf(format, a...)` | Printf with color |
| `Println(a...)` | Println with color |
| `Sprint(a...)` | Return colored string |
| `Sprintf(format, a...)` | Return formatted colored string |
| `Sprintln(a...)` | Return colored string with newline |
| `Add(attrs...)` | Add more attributes |
| `AddRGB(r, g, b)` | Add RGB foreground |
| `AddBgRGB(r, g, b)` | Add RGB background |
| `DisableColor()` | Disable color for this instance |
| `EnableColor()` | Enable color for this instance |

### Helper Functions

| Function | Returns |
|----------|---------|
| `Black/Red/Green/Yellow/Blue/Magenta/Cyan/White(format, a...)` | Prints colored text |
| `HiBlack/HiRed/HiGreen/HiYellow/HiBlue/HiMagenta/HiCyan/HiWhite(format, a...)` | Prints hi-intensity colored text |
| `BlackString/RedString/...String(format, a...)` | Returns colored string |
| `HiBlackString/HiRedString/...String(format, a...)` | Returns hi-intensity colored string |

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🙏 Acknowledgments

- Built with [go-colorable](https://github.com/mattn/go-colorable) for Windows support
- Inspired by the need for beautiful terminal output

---

<p align="center">
  Made with ❤️ and lots of 🎨
</p>

