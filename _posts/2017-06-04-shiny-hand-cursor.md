---
layout: post
title: How to change hover cursor to pointer in R Shiny
description: Just a quick writeup, since it apparently doesn't exist anywhere else on the internet.
comments: true
published: true
---

Insert the following tag into your UI:

```
shinyUI(

	fluidPage(
	
		fluidRow(
		
			plotOutput("main_plot", click = "plot_click"),
			
			##### INSERT THIS TAG ######
			tags$head(tags$style( ######
				'#main_plot {     ######
				cursor: pointer;  ######
				}'))              ######
			############################
			
		)
	
	)

)

```