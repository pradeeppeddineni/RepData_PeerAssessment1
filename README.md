#pradeep peddineni
#RepData_PeerAssessment1
#12/22/2016
PC-Windows7/64/R3.3.2/

Hello All,


While working with this assignment I had couple of outstanding challanges, i did figure out other ways but, if u have time please comment down these issues 

 keep_md: true
 
issue using "keep_md: true" 

statement Error in yaml::yaml.load(enc2utf8(string), ...) : Scanner error: mapping values are not allowed in this context at line 4, column 23 Calls: ... yaml_load_utf8 -> mark_utf8 -> -> .Call Execution halted

So instead i have used render func to get the .md file.
library(rmarkdown) render("PA1_template.Rmd", md_document())

-----------------------------
I have posted a thread for second issue..
https://www.coursera.org/learn/reproducible-research/peer/gYyPt/course-project-1/discussions/threads/pq_tysg4EeaQDgq_dR_6Tg


for the assignment for mean and median i am trying to use ggplot to add lines for mean and median, but the legend is missing. for vertical line i know that we have to add manually. i have trying to add the variable value as legend couldn't succeed..! I have been trying to achieve below legend.

(legend in above link)

mean_value = round(mean(x), 1)

median_value = round(median(x), 1)

a <- ggplot(totalSteps,show_guide=T,aes(x = steps))+ggtitle("Histogram of daily steps") +xlab("Steps (binwidth 2000)") +geom_histogram(binwidth = 2000)+geom_vline(xintercept = median_value,lwd = 5, col = 'red')+geom_vline(xintercept = mean_value,lwd = 2, col = 'blue')

any ideas ?



Thanks & Regards,
Pradeep Peddineni.



