---
title: "Turning COVID-19 into a data visualization exercise for your students"
categories:
 - Tools & Technology
tags:
 - social science
 - teaching
 - software
 - tools
 - data visualization
 - covid
header:
  teaser: /docs/posts_images/johns-hopkins-dashboard.png
toc: true
---

> This post originally appeared on [SAGE Ocean](https://ocean.sagepub.com/blog/tools-and-tech/turning-covid-19-into-a-data-visualization-exercise-for-your-students)

We will emerge from this pandemic with a better understanding of the world and an improved ability to teach others about it. For now, we need to be continuously analyzing the data and thinking about the lessons we can learn and apply. Here’s how you can join in!

At SAGE, we have been working with academics around improving and sharing teaching resources, especially for quantitative and computational methods in social sciences. Besides the [mass remote and emergency teaching experiment happening right now](https://er.educause.edu/articles/2020/3/the-difference-between-emergency-remote-teaching-and-online-learning), one of the positive things we can already identify and reuse to improve learning in methods courses is the glut of data visualizations. The absolute advantage here is that all these visualizations are produced (almost always) with the same raw input, telling a variety of different stories. What better way to explain the different uses and impact of visualizations and the use of different tools to students than examples based on the same data?  

For this blog, we thought we would make a start collating the variety of plots and multi-panels grouped based on the tools and skills required to create them. We’ve also included further resources for the type of visuals we discuss or introductory materials around the tools used to create them. We hope these will be useful for teachers and students who want to learn more or use different visualization examples in their methods courses. 

## 1. Mapping the raw numbers to follow live data

{% include figure image_path="/docs/posts_images/johns-hopkins-dashboard.png" alt="Johns Hopkins Coronavirus Resource Dashboard screenshot taken on 4/1/2020" caption="Johns Hopkins Coronavirus Resource Dashboard screenshot taken on 4/1/2020" %}


While it’s an impressive effort to pull together live data from various sources, and the dashboard makes it almost effortless to follow the spread of the virus based on the reported numbers of infected people across the world, it is only that. It is not easy to draw many conclusions from these types of dashboards, and the red bubbles across the world could be visually misleading, especially when areas are more densely populated and so larger absolute numbers might convey wider spread, when in fact it’s inaccurate. This is pretty much like harvesting the wheat and selling it by the ton. You’ve got the wheat grains out of the field and into the barn, which you know is useful, but there isn’t much you can do with it if you don’t have a mill and some knowledge around making the flour and potentially yeast for something more easily consumable, like bread. 

**Pros**: Interactive, can be live, multi-panel, high-level view of the raw figures.

**Cons**: More useful when scaled to location or in this case the population; requires standard reporting across all geo locations otherwise hard to visualize missing data.

**Live map**: [here](https://coronavirus.jhu.edu/map.html).

**Data** available in this [GitHub repository](https://github.com/CSSEGISandData/COVID-19).

**Cite as**: Dong E, Du H, Gardner L. An interactive web-based dashboard to track COVID-19 in real-time. Lancet Infect Dis; published online Feb 19. https://doi.org/10.1016/S1473-3099(20)30120-1.

#### Resources:

  -  Going one step further and making your dashboard a bit more useful from [information is beautiful](https://informationisbeautiful.net/visualizations/covid-19-coronavirus-infographic-datapack/), and with many more details from [Max Roser and team](https://ourworldindata.org/coronavirus) as we are learning the best ways to convey live data to an increasingly more worried world.

  -  Noting that these numbers are based on positive tests, and different countries ramped up or de-escalated testing differently, this [FiveThirtyEight article](https://fivethirtyeight.com/features/coronavirus-case-counts-are-meaningless/) estimates various scenarios.

  -  Similar dashboards can be created with [Tableau Public](https://public.tableau.com/profile/covid.19.data.resource.hub#!/vizhome/COVID-19Cases_15840488375320/COVID-19Cases).

  -  Other dashboards and panels that you could easily create without advanced coding skills with [Datawrapper](https://blog.datawrapper.de/coronaviruscharts/) (including the famous cumulative cases by country from first known patients).

  -  [Learn ArcGIS](https://learn.arcgis.com/en/) and notes on [mapping covid-19 with ArcGIS](https://www.esri.com/arcgis-blog/products/product/mapping/mapping-coronavirus-responsibly/).

## 2. Using R and Shiny to interact with the visualizations

{% include figure image_path="/docs/posts_images/r-shiny-covid-1.png" alt="Credit Joachim Gassen - https://joachim-gassen.github.io/tidycovid19/" caption="Credit Joachim Gassen - https://joachim-gassen.github.io/tidycovid19/" %}

{% include figure image_path="/docs/posts_images/r-shiny-covid-2.png" alt="Credit Tinu Schneider, 2020. Code is on Github. This work is licensed under a Creative Commons Attribution-ShareAlike 4.0 International License" caption="Credit Tinu Schneider, 2020. Code is on Github. This work is licensed under a Creative Commons Attribution-ShareAlike 4.0 International License" %}

The beauty of using R and being really proficient with it is that you can quickly put together an interactive web interface for others to play with. This can be done with the open-source R package — [Shiny](https://rstudio.com/products/shiny/). For example, the most popular shared graphs in the news have been the ones around flattening the curve and aligning the trajectories of the virus spreading by country. But as you will know, the visualization can be sensationalized when different defaults are set. With this Shiny app from [Joachim Gassen](https://joachim-gassen.github.io/), you can move the dials and choose the variables to be displayed. Similarly, with this other [Shiny app](https://tinu.shinyapps.io/Flatten_the_Curve/) from [Tinu Schneider](https://github.com/tinu-schneider), you can adjust the defaults and see how the curve could flatten.

Going one step further, you can also use Shiny to create interactive simulations, like [this one](https://alhill.shinyapps.io/COVID19seir/) from [Alison Hill](https://twitter.com/alison_l_hill), a research fellow at Harvard, looking at the spread and the healthcare capacity. She also included a useful tutorial.

{% include figure image_path="/docs/posts_images/r-shiny-covid-2.png" alt="Credit Alison Hill. Simulation shows modelling COVID-19 spread vs healthcare capacity" caption="Credit Alison Hill. Simulation shows modelling COVID-19 spread vs healthcare capacity" %}

**Pros**: Open-source, can be replicated, interactive, can adjust the defaults

**Cons**: Requires some coding experience in R

**Data** and associated code available [here](https://joachim-gassen.github.io/tidycovid19/) for the trajectories by country, [here](https://github.com/tinu-schneider/Flatten_the_Curve) for flattening the curve, and [here](https://github.com/alsnhll/SEIR_COVID19) for the hospital capacity simulations. 

#### Resources: 

  -  RStudio blog on using R, tidyverse packages and RECON libraries [to compile and visualize covid19 data](https://rviews.rstudio.com/2020/03/05/covid-19-epidemiology-with-r/).

  -  Maja Zaloznik’s Intro to R. Access the [slides](https://majazaloznik.github.io/2019-03-sage/presentations/2019-03-12-Intro-toR-webinar.html#1) or watch the [webinar](https://www.youtube.com/watch?v=al0rqd7jT3U&feature=youtu.be).

  -  The Carpentries’ [R for Social Scientists](https://datacarpentry.org/r-socialsci/) training, which includes data viz with ggplot.

  -  Cool [intro workshop to using ggplot in R](https://youtu.be/h29g21z0a68).

  -  A train-the-trainer session on how to teach [Shiny from RStudio](https://github.com/rstudio-education/teach-shiny).

  -  More examples of visualizations in [R from RStudio](https://shiny.rstudio.com/gallery/) and [Rittman Mead](https://www.r-graph-gallery.com/), and a [primer](https://rstudio.cloud/learn/primers/3) on data visualization also from RStudio.

  -  Improve your data visualizations with more recipes and loads of examples from this [R Graphics Cookbook](https://r-graphics.org/).

  -  Full course materials using R: [Modeling Criminological Data](https://jjmedinaariza.github.io/modelling_book/) from the University of Manchester or this workshop on [Getting Started with R](https://rcatlord.github.io/GSinR/) from Réka Solymosi, Henry Partridge and Sam Langton.

## 3. Using python with matplotlib to visualize tweets

Yes, these graphs require much more work and a team of about nine researchers to collect the data, conduct analyses and visualize it properly. The Computational Story Lab at University of Vermont collected tweets in more than 20 languages related to COVID-19 and used a variety of tools to get to these visualizations: unix, matplotlib, mongodb, gitlab, and ‘an exceedingly small batch of artisanal matlab by the artist Peter Sheridan Dodds’, @peterdodds (according to Chris Danford). The easy to digest summary [here](https://twitter.com/compstorylab/status/1243659358107467782), and [full paper with code](http://compstorylab.org/covid19ngrams/) on gitlab.

**Pros**: Can do advanced and multi-panel visualizations.

**Cons**: You need the skills to use these tools.

**Data** available in [gitlab](https://gitlab.com/compstorylab/covid19ngrams/).

**Cite as**: Alshaabi, T., Minot, J.R., Arnold, M.V., Adams, J.L., Dewhurst, D.R., Reagan, A.J., Muhamad, R., Danforth, C.M., & Dodds, P.S. (2020). How the world's collective attention is being paid to a pandemic: COVID-19 related 1-gram time series for 24 languages on Twitter. https://arxiv.org/abs/2003.12614.

#### Resources:

  -  How to use [python to gather COVID-19 data](https://towardsdatascience.com/gather-all-the-coronavirus-data-with-python-19aa22167dea).

  -  A basic [mapping of #covid19 cases in the UK with python](https://github.com/DavidBeavan/coronavirus_covid-19/blob/master/coronavirus_covid-19_england_map.ipynb).

  -  SAGE Campus: [Introduction to Python for social scientists](https://campus.sagepub.com/introduction-to-python-for-social-scientists?_ga=2.177553061.169058779.1610221959-926146671.1607529470).

  -  Phillip Brooker’s [Programming with Python for Social Science](https://uk.sagepub.com/en-gb/eur/programming-with-python-for-social-scientists/book259581?_ga=2.188207656.169058779.1610221959-926146671.1607529470).

  -  All [types of charts with Python](https://python-graph-gallery.com/) explained.

  -  [100 tips and tricks for working with pandas](https://www.dataschool.io/python-pandas-tips-and-tricks/) from Data School.

  -  [Simple ways to improve your matplotlib](https://towardsdatascience.com/simple-ways-to-improve-your-matplotlib-b64eebccfd5) from Kimberly Fessel.

  -  [Visualizing with matplotlib](https://jakevdp.github.io/PythonDataScienceHandbook/04.00-introduction-to-matplotlib.html) excerpt and code from O'Reilly Python Data Science Handbook by Jake VanderPlas.

## 4. Visualizing predictions and simulations (advanced)

This requires a whole other post, but I wanted to mention a few examples we came across that sparked our attention and that we thought could be a good way to entice anyone to learn advanced simulation methods: 

  -  Going deep with the [Bayesian scientist extracting patterns from real and synthetic models](https://advances.sciencemag.org/content/6/5/eaav6971).

  -  On flattening the curve, this [plot is interactive](http://gabgoh.github.io/COVID/index.html.), using RK4 for analysis and built with Svelte. 

## More resources:

Before you build another graph, especially for an ongoing event, where communication of risk and uncertainty is critical to saving lives, we definitely recommend considering some data visualization basics, for example:

  -  these [tips](https://medium.com/nightingale/ten-considerations-before-you-create-another-chart-about-covid-19-27d3bd691be8) from Amanda Makulec.

  -  Andy Kirk’s [recommendations for better data visualizations](https://www.methodspace.com/data-visualization-series-with-andy-kirk/), or his brilliant chartmaker for picking the right tool.

  -  [Visualizations can illuminate, but they can also be misleading](https://builtin.com/data-science/data-visualization-lessons-pandemic). A discussion on visualizing uncertainty across all COVID-19 charts. 

A final point on data visualizations from our friends at [ADDTWO](https://www.addtwodigital.com/): although seems trivial, the main thing students struggle with is the last step - making their graph look ‘polished’! Why is this so hard? While accurate representations are critical and even when many are able to pick the right chart types, data visualizations are stories, and the design and the use of colors and sizes on graphs is similarly important. Sometimes, the tools you use are either limited or not as user friendly on the design-and-polish steps. The team at ADDTWO recommends exporting (whenever possible) your visuals as .svg and further sharpening the design with any illustrator apps (Adobe Illustrator, figma and others).

Which other data visualization examples you will be using for your next workshop or module? What are your top tips? 