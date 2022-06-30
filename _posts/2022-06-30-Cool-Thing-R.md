ST558_Blog3
================
2022-06-30

One of the coolest thing I’ve learned about programming in R is its
powerful packages, which exist to do almost anything. For example, I’d
like to show the coronavirus cases by country in the world map. I can
just read in the world map data set, which includes the longitude,
latitude and country names.

``` r
# Read in the world map
mapdata <- map_data("world")
head(mapdata)
```

    ##        long      lat group order region subregion
    ## 1 -69.89912 12.45200     1     1  Aruba      <NA>
    ## 2 -69.89571 12.42300     1     2  Aruba      <NA>
    ## 3 -69.94219 12.43853     1     3  Aruba      <NA>
    ## 4 -70.00415 12.50049     1     4  Aruba      <NA>
    ## 5 -70.06612 12.54697     1     5  Aruba      <NA>
    ## 6 -70.05088 12.59707     1     6  Aruba      <NA>

Then, I read in the coronavirus cases from API.

``` r
covid_summary <- get_Data("/summary")$Countries %>% as_tibble()
```

After combine the coronavirus and world map data sets. I can simply
create a worldwide coronavirus map by ggplot.

``` r
# Combine the map and covid_summary data sets 
mapData <- left_join(mapdata, covid_summary, by = c("region" = "new_Countries"))

# Remove the rows which do not contain total confirmed cases numbers 
mapdata1 <- mapData %>% filter(!is.na(mapData$TotalConfirmed))
```

``` r
ggplot(mapdata1, aes(x= long, y =lat, group = group)) +
  geom_polygon(aes(fill = TotalConfirmed), color = "darkgreen") + 
  scale_fill_gradient(name = "Cases", low='#EEEEEE', high='darkgreen', na.value = "grey") +
  theme(axis.text.x = element_blank(),
        axis.text.y = element_blank(),
        axis.ticks = element_blank(),
        axis.title.y=element_blank(),
        axis.title.x=element_blank(),
        rect = element_blank()) +
  labs(title = "Coronavirus Worldwide")
```

![](C:\Harry\for%20Lan\ST558\blog\oaktreetrail.github.io_posts\2022-06-30-Cool-Thing-R_files/figure-gfm/unnamed-chunk-7-1.png)<!-- -->

This map shows us that the United States of America has the largest
total confirmed cases, followed by India and Brazil.
