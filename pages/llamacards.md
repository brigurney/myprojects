---
layout: page
title: Llama Card Game Simulation
description: Finding the right strategy for the LLAMA Card Game via simulation
---

This code is to simulate playing the LLAMA Card Game. 
Instructions for how to play can be found at [this website](https://www.amigo.games/content/ap/rule/19420--031-2019-Lama_Manual_002_LAYOUT[1].pdf)

### Functions
First, I will create some useful functions.
The first, getpoints, will take a player's hand and count how many points that hand is worth.
```{r}
getpoints <- function(hand) {
  hand[hand == 7] <- 10
  points <- sum(unique(hand))
  return(points)
}
```

Next,
