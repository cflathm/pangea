# PANGEA: Power ANalysis for GEneral ANOVA Designs

PANGEA is a flexible R-based tool for performing power analysis across a wide variety of ANOVA designs, including crossed or nested factors and fixed or random effects. It runs as a [Shiny](https://shiny.posit.co/) web app and can be launched locally using R from the command line.

You can also try the hosted version here:  
➡️ https://jakewestfall.shinyapps.io/pangea

---

## 🖥️ Run Locally (macOS Terminal, No RStudio)

This guide walks you through installing R and running PANGEA locally using only the macOS Terminal (no RStudio required).

---

### ✅ Requirements

- macOS (These instrucitons are for Mac, you can do this elsewhere)
- R (version ≥ 4.0)
- Internet access to install R packages
- Terminal

---

### 📥 Step 1: Install R

1. Go to [https://cran.r-project.org](https://cran.r-project.org)
2. Click **"Download R for macOS"**
3. Download the latest `.pkg` file (e.g., `R-4.x.x.pkg`)
4. Open it and follow the installer prompts

After installation, the `R` command will be available in your terminal.

---

### 📁 Step 2: Clone or Download This Repository

#### Option A: Clone with Git

```bash
git clone https://github.com/jake-westfall/pangea.git
cd pangea
```

#### Option B: Manual Download

1. Click the green **“Code”** button → **“Download ZIP”**
2. Unzip the folder
3. In Terminal, navigate to the folder:

```bash
cd ~/path/to/pangea
```

Make sure you see the following files in the directory:

```
global.R
server.R
ui.R
```

---

### 💻 Step 3: Start R in the Terminal

```bash
R
```

You should see an R prompt:

```
R version 4.x.x (202x-xx-xx) -- "..."
Type 'q()' to quit R.
>
```

---

### 📦 Step 4: Install Required Packages

Only do this the first time. In the R prompt, run:

```r
install.packages("shiny")
install.packages("dplyr")
install.packages("purrr")
install.packages("rlang")
install.packages("tidyr")
```

---

### 🚀 Step 5: Run the App

From the same R prompt, run:

```r
shiny::runApp(".")
```

This will launch the app in your default web browser.

---

### ⏹️ Step 6: Stop the App and Exit

- In the Terminal, press `Ctrl + C` to stop the app
- In R, type:

```r
q()
```

---

## 🛠️ Troubleshooting

| Problem                          | Solution                                                       |
|----------------------------------|----------------------------------------------------------------|
| `package not found`              | Run `install.packages("missing_package")`                      |
| `shiny not found`                | Run `install.packages("shiny")`                                |
| App does not launch              | Make sure you're in the folder with `global.R`, `ui.R`, `server.R` |
| Browser doesn’t open            | Copy the URL printed in the terminal and open it manually      |

---

## 🧾 License

MIT License. See [LICENSE](LICENSE) for details.

---

## 🙋 Author

Developed by [Jake Westfall](https://jakewestfall.org).

Questions or suggestions? Feel free to open an issue or fork the repository.
