# Tableau Story of NYC Citibike

The following sections each describe a page of the tableau story found [here](https://public.tableau.com/views/bikesharing_module15challenge/Story1?:language=en-US&publish=yes&:display_count=n&:origin=viz_share_link). We explored Citibike data, a service that rents out bikes, in New York City.  

### Page 1  

> Most trips are short (under 30 min) and on weekdays around commute hours  

At the top of this page is a graph of the number of bike rentals that went for a certain duration of time. The time is a bit difficult to read: each vertical section of the graph represents an hour mark of a trip duration. Then, the x-axis of each vertical strip is the minute mark of a trip duration. So, the left strip represents trips that went from 0-59 minutes, the middle strip represents trips that went from 60-119 minutes, and the right strip represents trips that went from 120-179 minutes. Additional hour mark durations can be toggled to the right. The count of trips is plotted on a log scale so the longer trips are still visible on the plot.  

The bottom graph shows a heatmap of the number of trips initiated at a clock hour by day of the week.  

From the two graphs, we can see that most trips are short: about 150,000 trips only took 5 minutes. We can see the number of trips decreases as a power law with increasing duration of time. Most of these trips occur during commuting hours during the week day (7-9 am and 5-7 pm). However, there are still lots of bike rentals during the weekend days and weekday afternoons. 

### Page 2  

> Short trip users are subscribers, mostly for commuting. Longer trip users are mostly customers  

The top graph here is similar to the previous top graph: the number of rentals per trip duration on a log scale. This time, it is further subdivided into the type of renter: a subscriber (one who pays monthly for unlimited uses in the month) or a customer (one who pays per each use).  

The bottom graph is also split by renter type but shows the number of rentals from a specific starting time of day.  

As one would expect, subscribers use the bikes for short commutes. The number of rentals spikes during commuting hours for subscribers, which are also likely to be short trips in the top graph. Customer rentals plateau (rather than peak) with trips between 8-30 minutes, though are still outnumbered by suscriber use at these durations. Only beyond 45 minute durations do customer rentals out-number subscriber rentals. These customer trips are fairy consisten throughout daylight hours, with slight preference to the afternoon and early evening.  

### Page 3  

> "Customers" take longer duration trips and take the bikes farther than "subscribers"  

This page has 3 graphs stacked together. At the top is a graph of the median (the median was chosen to decrease noise during less-used times of the day/night) distance in miles of bike trips started at a specific hour. The distance is calculated between the start and end locations of the bike rental (and does account for the curvature of the Earth, though this isn't too necessary at these scales). As such, it is not the total distance the bike was ridden, but gives a vague idea for how far the median person traveled (for example, a sight seeing tour that begins and ends at the same place would register as 0 distance). It is split by renter type.  

The middle graph is the median duration of trips started at the hour noted on the x-axis. Again, the graph is split between renter type.  

The bottom graph is a simple ratio of the above two graphs, since speed is distance over time. Again, the distance is simply between the endpoints so this isn't a true speed of each rental.  

This page serves to highlight what we learned on the previous page: customers take longer trips. Along with the longer trips, the customer type of renters tend to go farther.  

### Page 4  

> Men make up the bulk of the users. Ungendered users take longer trips  

On this page are graphs similar to those on page 2 but broken up by user gender rather than renter type.  

Men take more trips than women, who take more trips than users with an unknown gender (also referred to as ungendered here).  

What's of especially interesting note here is the shapes of the lines on the top graph. Both lines for the men and women renters show the peak at short durations that then falls off in a power law; the line for the ungendered plateaus between 8-30 minutes. If you'll recall, the customer type of renter had that same plateau shape. We posit that half (from the counts of the plateaus) of the customer type do not fill out the gender field when signing up. Therefore, when looking at visualizations split by gender, the ungendered serve as a proxy for the customer type of renter.  

### Page 5  

> Men take shorter trips. Ungendered users go farther and longer.  

This page has similar graphs to page 3 but broken up by user gender rather than renter type.  

The ungendered users go farther and go longer than men and women, which is likely an artefact of the connection between customer types and unknown genders discussed above.  

More interestingly, women take longer trips and go farther than men on a median basis. From the previous page's bottom graph, though, the total number of men's trips out-number the number of women's trips by a factor of 2-3 at most starting times. As such, this should be investigated farther and with caution since the median statistic may be confusing conclusions.  

### Page 6

> Longer trips tends to be on the outskirts of downtown  

This page includes two sets of maps. Each set maps the ending location of a bike rental; the ending location was chosen because there were more trips that ended on the outskirts of downtown than started there (which is something of a quandary itself to be investigated another time). Each set of maps is split by gender, recalling that the ungendered also serves as a proxy for the customer type. The top graph is color-coded by the median duration of each rental ending at that location. The bottom graph is color-coded by the median distance between the starting location and ending location at that ending location.  

The first thing to notice between the sets of graphs is that the farther trips take longer. Though obvious, it explains matching aspects of the two sets of maps.  

From the two sets of maps, men take more trips both to and within the outskirts of the city than women. For example, in the northeast, there are more dots displaying short duration trips and long duration trips for men than women. Further, no trips for women ended across the river to the west.  

On these maps, the ungendered serve as a proxy for the customer type of renter. Between the top and bottom graphs, the colors indicate that the trips by the ungendered skew away from the lower quartiles of values. This confirms what we discussed earlier that the customer-type renters typically went longer and farther than the subscribers.  

## Summary  

In this story, we've gone through a brief analysis of rental bike data in NYC. Overall, subscribers dominate bike usage for short commuting trips, less than 15 minutes in duration. Customers utilize bike rentals for longer trips, likely for exploring the city. Furthermore, men rent bikes more than women do.  

Unfortunately, data was not collected that tracked actual distance each bike was taken. While attempts were made to get a vague understanding of this by taking the distance between starting and ending locations, the true distance data for investigating, e.g., sight-seeing remains inaccessible and conclusions incomplete. 
