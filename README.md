# 🎨 Color

A powerful and elegant Go package for colorful terminal output. Add vibrant colors, text styles, and formatting to your CLI applications with ease.

![Go Version](https://img.shields.io/badge/Go-1.18+-00ADD8?style=flat&logo=go)
![License](https://img.shields.io/badge/License-MIT-22c55e)
![Build](https://img.shields.io/badge/Build-Passing-22c55e)
![Coverage](https://img.shields.io/badge/Coverage-95%25-22c55e)

```
🔴🟠🟡🟢🔵🟣⚪⚫ Standard Colors
🔴🟠🟡🟢🔵🟣⚪⚫ Hi-Intensity Colors  
████████████████ RGB True Color Support
```

## ✨ Features

- 🌈 **16 Standard Colors** - 8 basic + 8 high-intensity foreground colors
- 🖼️ **Background Colors** - Full background color support
- 🎯 **24-bit True Color (RGB)** - Millions of colors at your fingertips
- ✍️ **Text Styles** - Bold, Italic, Underline, Strikethrough, and more
- 🔧 **Flexible API** - Multiple ways to apply colors
- 🖥️ **Cross-Platform** - Works on Windows, macOS, and Linux
- 🚫 **NO_COLOR Support** - Respects the [NO_COLOR](https://no-color.org/) standard

## 🖼️ Preview

```
┌─────────────────────────────────────────────────────────────────┐
│                                                                 │
│  ████ ERROR    Something went wrong!                           │
│  ████ WARNING  Check your configuration                        │
│  ████ SUCCESS  Operation completed                              │
│  ████ INFO     Processing your request                          │
│  ████ DEBUG    Variable x = 42                                  │
│  ████ TRACE    Entering function main()                        │
│                                                                 │
│  ▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓▓ RGB Gradient Support                     │
│  ░░░░░░░░░░░░░░░░░░░░ Background Colors                        │
│                                                                 │
└─────────────────────────────────────────────────────────────────┘
```

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

| Color | Standard | Badge | Hi-Intensity | Badge |
|-------|----------|-------|--------------|-------|
| ⬛ Black | `FgBlack` | ![Black](https://img.shields.io/badge/■-000000?style=flat-square) | `FgHiBlack` | ![HiBlack](https://img.shields.io/badge/■-555555?style=flat-square) |
| 🟥 Red | `FgRed` | ![Red](https://img.shields.io/badge/■-cc0000?style=flat-square) | `FgHiRed` | ![HiRed](https://img.shields.io/badge/■-ff0000?style=flat-square) |
| 🟩 Green | `FgGreen` | ![Green](https://img.shields.io/badge/■-00cc00?style=flat-square) | `FgHiGreen` | ![HiGreen](https://img.shields.io/badge/■-00ff00?style=flat-square) |
| 🟨 Yellow | `FgYellow` | ![Yellow](https://img.shields.io/badge/■-cccc00?style=flat-square) | `FgHiYellow` | ![HiYellow](https://img.shields.io/badge/■-ffff00?style=flat-square) |
| 🟦 Blue | `FgBlue` | ![Blue](https://img.shields.io/badge/■-0000cc?style=flat-square) | `FgHiBlue` | ![HiBlue](https://img.shields.io/badge/■-0000ff?style=flat-square) |
| 🟪 Magenta | `FgMagenta` | ![Magenta](https://img.shields.io/badge/■-cc00cc?style=flat-square) | `FgHiMagenta` | ![HiMagenta](https://img.shields.io/badge/■-ff00ff?style=flat-square) |
| 🩵 Cyan | `FgCyan` | ![Cyan](https://img.shields.io/badge/■-00cccc?style=flat-square) | `FgHiCyan` | ![HiCyan](https://img.shields.io/badge/■-00ffff?style=flat-square) |
| ⬜ White | `FgWhite` | ![White](https://img.shields.io/badge/■-cccccc?style=flat-square) | `FgHiWhite` | ![HiWhite](https://img.shields.io/badge/■-ffffff?style=flat-square) |

### Background Colors

| Color | Standard | Badge | Hi-Intensity | Badge |
|-------|----------|-------|--------------|-------|
| ⬛ Black | `BgBlack` | ![BgBlack](https://img.shields.io/badge/████-000000?style=flat-square) | `BgHiBlack` | ![BgHiBlack](https://img.shields.io/badge/████-555555?style=flat-square) |
| 🟥 Red | `BgRed` | ![BgRed](https://img.shields.io/badge/████-cc0000?style=flat-square) | `BgHiRed` | ![BgHiRed](https://img.shields.io/badge/████-ff0000?style=flat-square) |
| 🟩 Green | `BgGreen` | ![BgGreen](https://img.shields.io/badge/████-00cc00?style=flat-square) | `BgHiGreen` | ![BgHiGreen](https://img.shields.io/badge/████-00ff00?style=flat-square) |
| 🟨 Yellow | `BgYellow` | ![BgYellow](https://img.shields.io/badge/████-cccc00?style=flat-square) | `BgHiYellow` | ![BgHiYellow](https://img.shields.io/badge/████-ffff00?style=flat-square) |
| 🟦 Blue | `BgBlue` | ![BgBlue](https://img.shields.io/badge/████-0000cc?style=flat-square) | `BgHiBlue` | ![BgHiBlue](https://img.shields.io/badge/████-0000ff?style=flat-square) |
| 🟪 Magenta | `BgMagenta` | ![BgMagenta](https://img.shields.io/badge/████-cc00cc?style=flat-square) | `BgHiMagenta` | ![BgHiMagenta](https://img.shields.io/badge/████-ff00ff?style=flat-square) |
| 🩵 Cyan | `BgCyan` | ![BgCyan](https://img.shields.io/badge/████-00cccc?style=flat-square) | `BgHiCyan` | ![BgHiCyan](https://img.shields.io/badge/████-00ffff?style=flat-square) |
| ⬜ White | `BgWhite` | ![BgWhite](https://img.shields.io/badge/████-cccccc?style=flat-square) | `BgHiWhite` | ![BgHiWhite](https://img.shields.io/badge/████-ffffff?style=flat-square) |

### 🌈 RGB Color Examples

| Color Name | RGB Values | Badge | Code |
|------------|------------|-------|------|
| Coral | `255, 127, 80` | ![Coral](https://img.shields.io/badge/████-FF7F50?style=flat-square) | `color.RGB(255, 127, 80)` |
| Tomato | `255, 99, 71` | ![Tomato](https://img.shields.io/badge/████-FF6347?style=flat-square) | `color.RGB(255, 99, 71)` |
| Orange Red | `255, 69, 0` | ![OrangeRed](https://img.shields.io/badge/████-FF4500?style=flat-square) | `color.RGB(255, 69, 0)` |
| Gold | `255, 215, 0` | ![Gold](https://img.shields.io/badge/████-FFD700?style=flat-square) | `color.RGB(255, 215, 0)` |
| Lime Green | `50, 205, 50` | ![LimeGreen](https://img.shields.io/badge/████-32CD32?style=flat-square) | `color.RGB(50, 205, 50)` |
| Spring Green | `0, 255, 127` | ![SpringGreen](https://img.shields.io/badge/████-00FF7F?style=flat-square) | `color.RGB(0, 255, 127)` |
| Turquoise | `64, 224, 208` | ![Turquoise](https://img.shields.io/badge/████-40E0D0?style=flat-square) | `color.RGB(64, 224, 208)` |
| Deep Sky Blue | `0, 191, 255` | ![DeepSkyBlue](https://img.shields.io/badge/████-00BFFF?style=flat-square) | `color.RGB(0, 191, 255)` |
| Dodger Blue | `30, 144, 255` | ![DodgerBlue](https://img.shields.io/badge/████-1E90FF?style=flat-square) | `color.RGB(30, 144, 255)` |
| Royal Blue | `65, 105, 225` | ![RoyalBlue](https://img.shields.io/badge/████-4169E1?style=flat-square) | `color.RGB(65, 105, 225)` |
| Blue Violet | `138, 43, 226` | ![BlueViolet](https://img.shields.io/badge/████-8A2BE2?style=flat-square) | `color.RGB(138, 43, 226)` |
| Dark Orchid | `153, 50, 204` | ![DarkOrchid](https://img.shields.io/badge/████-9932CC?style=flat-square) | `color.RGB(153, 50, 204)` |
| Hot Pink | `255, 105, 180` | ![HotPink](https://img.shields.io/badge/████-FF69B4?style=flat-square) | `color.RGB(255, 105, 180)` |
| Deep Pink | `255, 20, 147` | ![DeepPink](https://img.shields.io/badge/████-FF1493?style=flat-square) | `color.RGB(255, 20, 147)` |
| Crimson | `220, 20, 60` | ![Crimson](https://img.shields.io/badge/████-DC143C?style=flat-square) | `color.RGB(220, 20, 60)` |
| Indian Red | `205, 92, 92` | ![IndianRed](https://img.shields.io/badge/████-CD5C5C?style=flat-square) | `color.RGB(205, 92, 92)` |
| Slate Blue | `106, 90, 205` | ![SlateBlue](https://img.shields.io/badge/████-6A5ACD?style=flat-square) | `color.RGB(106, 90, 205)` |
| Medium Purple | `147, 112, 219` | ![MediumPurple](https://img.shields.io/badge/████-9370DB?style=flat-square) | `color.RGB(147, 112, 219)` |
| Orchid | `218, 112, 214` | ![Orchid](https://img.shields.io/badge/████-DA70D6?style=flat-square) | `color.RGB(218, 112, 214)` |
| Plum | `221, 160, 221` | ![Plum](https://img.shields.io/badge/████-DDA0DD?style=flat-square) | `color.RGB(221, 160, 221)` |

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

### Rainbow Text Effect

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
}
```

### RGB Gradient Effects

```go
// Fire gradient: Red → Orange → Yellow
func fireGradient() {
    for i := 0; i < 20; i++ {
        r := 255
        g := min(255, i*12)
        color.RGB(r, g, 0).Print("█")
    }
    fmt.Println(" 🔥 Fire")
}

// Ocean gradient: Deep Blue → Cyan → Aqua
func oceanGradient() {
    for i := 0; i < 20; i++ {
        r := i * 5
        g := 100 + i*7
        b := 255
        color.RGB(r, g, b).Print("█")
    }
    fmt.Println(" 🌊 Ocean")
}

// Forest gradient: Dark Green → Lime
func forestGradient() {
    for i := 0; i < 20; i++ {
        r := i * 8
        g := 100 + i*7
        b := i * 3
        color.RGB(r, g, b).Print("█")
    }
    fmt.Println(" 🌲 Forest")
}

// Sunset gradient: Purple → Pink → Orange
func sunsetGradient() {
    for i := 0; i < 20; i++ {
        r := 128 + i*6
        g := i * 5
        b := 255 - i*8
        color.RGB(r, g, b).Print("█")
    }
    fmt.Println(" 🌅 Sunset")
}

// Neon gradient: Pink → Purple → Blue
func neonGradient() {
    for i := 0; i < 20; i++ {
        r := 255 - i*8
        g := i * 5
        b := 128 + i*6
        color.RGB(r, g, b).Print("█")
    }
    fmt.Println(" 💜 Neon")
}

// Gold gradient: Brown → Gold → Yellow
func goldGradient() {
    for i := 0; i < 20; i++ {
        r := 139 + i*5
        g := 90 + i*8
        b := i * 2
        color.RGB(r, g, b).Print("█")
    }
    fmt.Println(" ✨ Gold")
}
```

### All Colors Demo

```go
func showAllColors() {
    fmt.Println("\n╔════════════════════════════════════════╗")
    fmt.Println("║         STANDARD FOREGROUND            ║")
    fmt.Println("╠════════════════════════════════════════╣")
    
    color.Black("  ██ Black   ")
    color.Red("  ██ Red     ")
    color.Green("  ██ Green   ")
    color.Yellow("  ██ Yellow  ")
    color.Blue("  ██ Blue    ")
    color.Magenta("  ██ Magenta ")
    color.Cyan("  ██ Cyan    ")
    color.White("  ██ White   ")
    
    fmt.Println("\n╠════════════════════════════════════════╣")
    fmt.Println("║         HI-INTENSITY FOREGROUND        ║")
    fmt.Println("╠════════════════════════════════════════╣")
    
    color.HiBlack("  ██ HiBlack   ")
    color.HiRed("  ██ HiRed     ")
    color.HiGreen("  ██ HiGreen   ")
    color.HiYellow("  ██ HiYellow  ")
    color.HiBlue("  ██ HiBlue    ")
    color.HiMagenta("  ██ HiMagenta ")
    color.HiCyan("  ██ HiCyan    ")
    color.HiWhite("  ██ HiWhite   ")
    
    fmt.Println("\n╚════════════════════════════════════════╝")
}
```

### Background Colors Gallery

```go
func showBackgrounds() {
    fmt.Println("\n🎨 Background Color Combinations:\n")
    
    // Standard backgrounds with white text
    color.New(color.FgWhite, color.BgBlack).Println("   BgBlack   ")
    color.New(color.FgWhite, color.BgRed).Println("   BgRed     ")
    color.New(color.FgBlack, color.BgGreen).Println("   BgGreen   ")
    color.New(color.FgBlack, color.BgYellow).Println("   BgYellow  ")
    color.New(color.FgWhite, color.BgBlue).Println("   BgBlue    ")
    color.New(color.FgWhite, color.BgMagenta).Println("   BgMagenta ")
    color.New(color.FgBlack, color.BgCyan).Println("   BgCyan    ")
    color.New(color.FgBlack, color.BgWhite).Println("   BgWhite   ")
    
    // Hi-intensity backgrounds
    color.New(color.FgWhite, color.BgHiBlack).Println("   BgHiBlack   ")
    color.New(color.FgWhite, color.BgHiRed).Println("   BgHiRed     ")
    color.New(color.FgBlack, color.BgHiGreen).Println("   BgHiGreen   ")
    color.New(color.FgBlack, color.BgHiYellow).Println("   BgHiYellow  ")
    color.New(color.FgWhite, color.BgHiBlue).Println("   BgHiBlue    ")
    color.New(color.FgWhite, color.BgHiMagenta).Println("   BgHiMagenta ")
    color.New(color.FgBlack, color.BgHiCyan).Println("   BgHiCyan    ")
    color.New(color.FgBlack, color.BgHiWhite).Println("   BgHiWhite   ")
}
```

## 🎭 Theme Examples

### Cyberpunk Theme

```go
func cyberpunkTheme() {
    // Neon pink on dark
    title := color.New(color.Bold).AddRGB(255, 0, 128)
    // Electric blue
    accent := color.RGB(0, 255, 255)
    // Purple
    secondary := color.RGB(138, 43, 226)
    // Dark magenta background
    alert := color.New(color.FgWhite, color.Bold).AddBgRGB(75, 0, 130)
    
    title.Println("╔══════════════════════════════════╗")
    title.Println("║   🌆 CYBERPUNK TERMINAL v2.0     ║")
    title.Println("╚══════════════════════════════════╝")
    accent.Println(">>> System initialized...")
    secondary.Println(">>> Neural link established...")
    alert.Println("   ⚠ SECURITY BREACH DETECTED   ")
}
```

### Retro Terminal Theme

```go
func retroTheme() {
    // Classic green on black
    green := color.New(color.FgGreen)
    brightGreen := color.New(color.FgHiGreen, color.Bold)
    
    brightGreen.Println("┌────────────────────────────────┐")
    brightGreen.Println("│  RETRO TERMINAL OS v1.0        │")
    brightGreen.Println("└────────────────────────────────┘")
    green.Println("> READY.")
    green.Println("> LOAD \"PROGRAM\",8,1")
    brightGreen.Println("> SEARCHING FOR PROGRAM...")
    green.Println("> LOADING...")
    brightGreen.Println("> RUN")
}
```

### Dracula Theme

```go
func draculaTheme() {
    // Dracula color palette
    background := color.RGB(40, 42, 54)     // Dark
    foreground := color.RGB(248, 248, 242)  // Light
    comment := color.RGB(98, 114, 164)      // Purple-gray
    cyan := color.RGB(139, 233, 253)
    green := color.RGB(80, 250, 123)
    orange := color.RGB(255, 184, 108)
    pink := color.RGB(255, 121, 198)
    purple := color.RGB(189, 147, 249)
    red := color.RGB(255, 85, 85)
    yellow := color.RGB(241, 250, 140)
    
    pink.Println("🧛 Dracula Theme Colors:")
    purple.Println("   Purple for keywords")
    cyan.Println("   Cyan for classes")
    green.Println("   Green for strings")
    orange.Println("   Orange for constants")
    yellow.Println("   Yellow for warnings")
    red.Println("   Red for errors")
    comment.Println("   Gray for comments")
}
```

### Nord Theme

```go
func nordTheme() {
    // Nord color palette - Arctic, north-bluish colors
    polar1 := color.RGB(46, 52, 64)
    polar2 := color.RGB(59, 66, 82)
    snow1 := color.RGB(236, 239, 244)
    frost1 := color.RGB(143, 188, 187)  // Cyan
    frost2 := color.RGB(136, 192, 208)  // Light blue
    frost3 := color.RGB(129, 161, 193)  // Blue
    frost4 := color.RGB(94, 129, 172)   // Dark blue
    aurora1 := color.RGB(191, 97, 106)  // Red
    aurora2 := color.RGB(208, 135, 112) // Orange
    aurora3 := color.RGB(235, 203, 139) // Yellow
    aurora4 := color.RGB(163, 190, 140) // Green
    aurora5 := color.RGB(180, 142, 173) // Purple
    
    frost2.Println("❄️  Nord Theme - Arctic Colors")
    frost1.Println("   Frost: Icy cyan tones")
    frost3.Println("   Frost: Cool blue shades")
    aurora4.Println("   Aurora: Northern lights green")
    aurora5.Println("   Aurora: Mystical purple")
    aurora1.Println("   Aurora: Arctic red")
    aurora3.Println("   Aurora: Polar yellow")
}
```

### Monokai Theme

```go
func monokaiTheme() {
    // Monokai Pro colors
    yellow := color.RGB(255, 216, 102)
    orange := color.RGB(252, 151, 103)
    red := color.RGB(255, 97, 136)
    magenta := color.RGB(171, 157, 242)
    blue := color.RGB(120, 220, 232)
    green := color.RGB(169, 220, 118)
    
    yellow.Println("🎨 Monokai Theme")
    green.Println("   func main() {")
    blue.Println("       fmt.Println(")
    orange.Println("           \"Hello, World!\"")
    blue.Println("       )")
    green.Println("   }")
    red.Println("   // Error handling")
    magenta.Println("   // Keywords & types")
}
```

## 🎪 Fun Color Effects

### Animated Loading Spinner Colors

```go
func colorSpinner() {
    spinnerColors := []*color.Color{
        color.New(color.FgRed),
        color.New(color.FgYellow),
        color.New(color.FgGreen),
        color.New(color.FgCyan),
        color.New(color.FgBlue),
        color.New(color.FgMagenta),
    }
    frames := []string{"⠋", "⠙", "⠹", "⠸", "⠼", "⠴", "⠦", "⠧", "⠇", "⠏"}
    
    for i := 0; i < 30; i++ {
        c := spinnerColors[i%len(spinnerColors)]
        frame := frames[i%len(frames)]
        fmt.Printf("\r%s Loading...", c.Sprint(frame))
        time.Sleep(100 * time.Millisecond)
    }
    color.Green("\r✓ Complete!     \n")
}
```

### Matrix Rain Effect

```go
func matrixRain() {
    chars := "ｱｲｳｴｵｶｷｸｹｺｻｼｽｾｿﾀﾁﾂﾃﾄﾅﾆﾇﾈﾉﾊﾋﾌﾍﾎﾏﾐﾑﾒﾓﾔﾕﾖﾗﾘﾙﾚﾛﾜﾝ0123456789"
    green := color.New(color.FgGreen)
    brightGreen := color.New(color.FgHiGreen, color.Bold)
    
    for i := 0; i < 5; i++ {
        line := ""
        for j := 0; j < 40; j++ {
            char := string(chars[rand.Intn(len(chars))])
            if rand.Float32() < 0.1 {
                line += brightGreen.Sprint(char)
            } else {
                line += green.Sprint(char)
            }
        }
        fmt.Println(line)
    }
}
```

### Color Palette Generator

```go
func generatePalette(baseR, baseG, baseB int) {
    fmt.Println("\n🎨 Generated Color Palette:\n")
    
    // Lighter shades
    for i := 4; i >= 1; i-- {
        factor := 1.0 + float64(i)*0.15
        r := min(255, int(float64(baseR)*factor))
        g := min(255, int(float64(baseG)*factor))
        b := min(255, int(float64(baseB)*factor))
        color.RGB(r, g, b).Printf("████ RGB(%3d, %3d, %3d)\n", r, g, b)
    }
    
    // Base color
    color.RGB(baseR, baseG, baseB).Printf("████ RGB(%3d, %3d, %3d) ← Base\n", baseR, baseG, baseB)
    
    // Darker shades
    for i := 1; i <= 4; i++ {
        factor := 1.0 - float64(i)*0.15
        r := max(0, int(float64(baseR)*factor))
        g := max(0, int(float64(baseG)*factor))
        b := max(0, int(float64(baseB)*factor))
        color.RGB(r, g, b).Printf("████ RGB(%3d, %3d, %3d)\n", r, g, b)
    }
}

// Usage
generatePalette(66, 135, 245)  // Blue palette
generatePalette(245, 124, 66)  // Orange palette
generatePalette(102, 187, 106) // Green palette
```

### ASCII Art with Colors

```go
func colorfulBanner() {
    red := color.New(color.FgRed, color.Bold)
    orange := color.RGB(255, 165, 0)
    yellow := color.New(color.FgYellow, color.Bold)
    green := color.New(color.FgGreen, color.Bold)
    blue := color.New(color.FgBlue, color.Bold)
    purple := color.RGB(128, 0, 128)
    
    red.Println("   ██████╗ ██████╗ ██╗      ██████╗ ██████╗ ")
    orange.Println("  ██╔════╝██╔═══██╗██║     ██╔═══██╗██╔══██╗")
    yellow.Println("  ██║     ██║   ██║██║     ██║   ██║██████╔╝")
    green.Println("  ██║     ██║   ██║██║     ██║   ██║██╔══██╗")
    blue.Println("  ╚██████╗╚██████╔╝███████╗╚██████╔╝██║  ██║")
    purple.Println("   ╚═════╝ ╚═════╝ ╚══════╝ ╚═════╝ ╚═╝  ╚═╝")
}
```

## 🔢 256 Color Mode

```go
// 256 color mode uses extended color codes
// Foreground: 38;5;n where n is 0-255
// Background: 48;5;n where n is 0-255

func show256Colors() {
    fmt.Println("\n📊 256 Color Palette:\n")
    
    // Standard colors (0-15)
    fmt.Println("Standard Colors (0-15):")
    for i := 0; i < 16; i++ {
        fmt.Printf("\x1b[48;5;%dm  \x1b[0m", i)
    }
    fmt.Println()
    
    // 216 colors (16-231)
    fmt.Println("\n216 Colors (16-231):")
    for i := 16; i < 232; i++ {
        fmt.Printf("\x1b[48;5;%dm  \x1b[0m", i)
        if (i-15)%36 == 0 {
            fmt.Println()
        }
    }
    
    // Grayscale (232-255)
    fmt.Println("\nGrayscale (232-255):")
    for i := 232; i < 256; i++ {
        fmt.Printf("\x1b[48;5;%dm  \x1b[0m", i)
    }
    fmt.Println()
}
```

## 🎨 Popular Color Combinations

Here are some beautiful and commonly used color combinations:

| Style | Foreground | Background | Use Case |
|-------|------------|------------|----------|
| 🔴 Error | `FgWhite` | `BgRed` | Critical errors |
| 🟠 Warning | `FgBlack` | `BgYellow` | Warnings |
| 🟢 Success | `FgWhite` | `BgGreen` | Success messages |
| 🔵 Info | `FgWhite` | `BgBlue` | Information |
| 🟣 Debug | `FgWhite` | `BgMagenta` | Debug output |
| ⚫ Muted | `FgHiBlack` | - | Secondary text |
| 💡 Highlight | `FgBlack` | `BgHiYellow` | Important highlights |
| 🔗 Link | `FgCyan` + `Underline` | - | Links/URLs |
| 📝 Code | `FgHiWhite` | `BgHiBlack` | Code blocks |
| ⚡ Accent | `FgHiMagenta` + `Bold` | - | Emphasis |

```go
// Quick setup for common styles
var (
    ErrorStyle   = color.New(color.FgWhite, color.BgRed, color.Bold)
    WarningStyle = color.New(color.FgBlack, color.BgYellow)
    SuccessStyle = color.New(color.FgWhite, color.BgGreen)
    InfoStyle    = color.New(color.FgWhite, color.BgBlue)
    DebugStyle   = color.New(color.FgWhite, color.BgMagenta)
    MutedStyle   = color.New(color.FgHiBlack)
    LinkStyle    = color.New(color.FgCyan, color.Underline)
    CodeStyle    = color.New(color.FgHiWhite, color.BgHiBlack)
    AccentStyle  = color.New(color.FgHiMagenta, color.Bold)
)
```

## 🌟 Semantic Color Helpers

```go
// Create a complete set of semantic colors for your application
type Theme struct {
    Primary   *color.Color
    Secondary *color.Color
    Success   *color.Color
    Danger    *color.Color
    Warning   *color.Color
    Info      *color.Color
    Light     *color.Color
    Dark      *color.Color
    Muted     *color.Color
}

// Default theme
var DefaultTheme = Theme{
    Primary:   color.New(color.FgHiBlue, color.Bold),
    Secondary: color.New(color.FgHiBlack),
    Success:   color.New(color.FgHiGreen),
    Danger:    color.New(color.FgHiRed, color.Bold),
    Warning:   color.New(color.FgHiYellow),
    Info:      color.New(color.FgHiCyan),
    Light:     color.New(color.FgHiWhite),
    Dark:      color.New(color.FgBlack),
    Muted:     color.New(color.FgHiBlack, color.Faint),
}

// RGB Theme (Custom colors)
var ModernTheme = Theme{
    Primary:   color.RGB(99, 102, 241),   // Indigo
    Secondary: color.RGB(107, 114, 128),  // Gray
    Success:   color.RGB(34, 197, 94),    // Green
    Danger:    color.RGB(239, 68, 68),    // Red
    Warning:   color.RGB(234, 179, 8),    // Yellow
    Info:      color.RGB(6, 182, 212),    // Cyan
    Light:     color.RGB(248, 250, 252),  // Slate
    Dark:      color.RGB(15, 23, 42),     // Dark slate
    Muted:     color.RGB(148, 163, 184),  // Slate gray
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

## 🎨 Color Reference Card

```
╔═══════════════════════════════════════════════════════════════════════╗
║                        QUICK COLOR REFERENCE                          ║
╠═══════════════════════════════════════════════════════════════════════╣
║                                                                       ║
║  FOREGROUND          BACKGROUND          HI-INTENSITY                ║
║  ───────────         ───────────         ─────────────               ║
║  FgBlack    30       BgBlack    40       FgHiBlack    90              ║
║  FgRed      31       BgRed      41       FgHiRed      91              ║
║  FgGreen    32       BgGreen    42       FgHiGreen    92              ║
║  FgYellow   33       BgYellow   43       FgHiYellow   93              ║
║  FgBlue     34       BgBlue     44       FgHiBlue     94              ║
║  FgMagenta  35       BgMagenta  45       FgHiMagenta  95              ║
║  FgCyan     36       BgCyan     46       FgHiCyan     96              ║
║  FgWhite    37       BgWhite    47       FgHiWhite    97              ║
║                                                                       ║
║  STYLES              ESCAPE SEQUENCE                                  ║
║  ──────              ───────────────                                  ║
║  Bold       1        \x1b[1m                                          ║
║  Faint      2        \x1b[2m                                          ║
║  Italic     3        \x1b[3m                                          ║
║  Underline  4        \x1b[4m                                          ║
║  Blink      5        \x1b[5m                                          ║
║  Reverse    7        \x1b[7m                                          ║
║  Hidden     8        \x1b[8m                                          ║
║  Strike     9        \x1b[9m                                          ║
║  Reset      0        \x1b[0m                                          ║
║                                                                       ║
║  RGB FORMAT: \x1b[38;2;R;G;Bm (foreground)                            ║
║              \x1b[48;2;R;G;Bm (background)                            ║
║                                                                       ║
╚═══════════════════════════════════════════════════════════════════════╝
```

## 🌈 Example Output

When you run a colorful application, expect output like this:

```
┌──────────────────────────────────────────────────────────────┐
│                                                              │
│  🔴 [ERROR]   Connection failed: timeout after 30s          │
│  🟠 [WARN]    Memory usage at 85%                           │
│  🟢 [SUCCESS] Database migration completed                  │
│  🔵 [INFO]    Server started on port 8080                   │
│  🟣 [DEBUG]   Request ID: abc-123-def                       │
│  ⚪ [TRACE]   Entering function: handleRequest()            │
│                                                              │
│  ████████████████████ 100% Complete                         │
│                                                              │
│  Status: ✅ API  ✅ Database  ⚠️ Cache  ❌ Queue              │
│                                                              │
└──────────────────────────────────────────────────────────────┘
```

---

<p align="center">
  <img src="https://img.shields.io/badge/🔴-Red-ff0000" alt="Red">
  <img src="https://img.shields.io/badge/🟠-Orange-ff8c00" alt="Orange">
  <img src="https://img.shields.io/badge/🟡-Yellow-ffff00" alt="Yellow">
  <img src="https://img.shields.io/badge/🟢-Green-00ff00" alt="Green">
  <img src="https://img.shields.io/badge/🔵-Blue-0000ff" alt="Blue">
  <img src="https://img.shields.io/badge/🟣-Purple-8b00ff" alt="Purple">
</p>

<p align="center">
  <b>Made with ❤️ and lots of 🎨</b>
</p>

<p align="center">
  <sub>Paint your terminal with a rainbow of possibilities! 🌈</sub>
</p>

