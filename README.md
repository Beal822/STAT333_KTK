# Final Project for STAT333

This is my code repository for my final stats project in predictive Modeling (Stat 333)
ssh -T git@github.com
#Testing code updates

install.packages("Lahman")
library("Lahman")
str(Teams)

install.packages("dbplyr")
library("dbplyr")

# Filter for a specific range of years (e.g., 2000-2020)
yearly_stats <- Teams %>%
  filter(yearID >= 2000 & yearID <= 2020) %>%
  select(yearID, teamID, lgID, G, W, L, R, H, HR, SB, ERA)


view(yearly_stats)


# Importing team valuation data

team_valuation <- read.csv("C:/Users/brend/Downloads/SBR001-mlbte1.csv", header = TRUE, skip = 3, check.names = FALSE)
view(team_valuation)
