# assignment2
## Dataset
This is a Palmer Penguins dataset (`penguins.csv`) which contains measurements of penguins observed at the Palmer Station in Antarctica.
The dataset includes the following variables:

- `species` – penguin species (Adelie, Chinstrap, Gentoo)
- `island` – island where the penguin was observed
- `bill_length_mm` – bill length in millimeters
- `bill_depth_mm` – bill depth in millimeters
- `flipper_length_mm` – flipper length in millimeters
- `body_mass_g` – body mass in grams
- `sex` – penguin sex
- `year` – year of observation

Missing values are recorded as `NA`

## Data analysis report

**Script:** `qac380-assignment2.Rmd`

This R Markdown script loads `penguins.csv` and runs descriptive analyses:
1. Summary statistics (min, quartiles, median, mean, max) for the numeric
   measurements: bill length, bill depth, flipper length, and body mass.
2. Mean measurements grouped by species, to compare the three species.

The output is saved to `qac380-assignment2.html`.

## How to reproduce the analysis
1. Clone this repository to your computer.
2. Open `analysis.Rmd` in RStudio.
3. Make sure the working directory is the repository folder (the folder
   containing `penguins.csv`).
4. Knit the R Markdown file or run the chunks in order.

The script will read `penguins.csv` and regenerate `qac380-assignment2 `
with the same results.

##Run a linear regression: Does flipper length predict body mass?
model1 <- lm(body_mass_g ~ flipper_length_mm, data = penguins)
summary(model1)