---
title: "final_project_shiying"
output: html_document
---
<style>
body{ /* Normal */
font-size: 15px;
color: black;
}
write {  
line-height: 7em;
}
table { /* Table */
font-size: 12px;
}
h1 { /* Header 1 */
font-size: 30px;
}
h2 { /* Header 2 *
font-size: 26px;
}
h3 { /* Header 3 */
font-size: 22px;
}
code.r{ /* Code block */
font-size: 14px;
}
pre { /* Code block */
font-size: 14px
}
.main-container {
    width: 80%;
    max-width: unset;
}
</style>



```r
library(httr)
set_config(use_proxy(url="127.0.0.1",port=8668))
```


```r
library(dplyr)
library(ggplot2)
library(tidyverse) 
library(ggthemes)
library(reshape2)
library(lubridate) 
library("readxl")
```


```r
options("scipen"=100, "digits"=4)
```


How I get covid_us_county_level dataset

```r
#dataFiles <- lapply(Sys.glob("*.csv"), read.csv)
#covid_global<-bind_rows(dataFiles, .id = "column_label")
#covid_us_county_level<-covid_global %>% filter(Country_Region=="US")
#write.csv(x=covid_us_county_level, file="covid_us_county_level")
```


```r
covid_us_county_level<-read.csv("covid_us_county_level")
```

```
## Warning in file(file, "rt"): cannot open file 'covid_us_county_level': No such file or directory
```

```
## Error in file(file, "rt"): cannot open the connection
```


```r
read.csv("trump 2020 presidential election rallies.csv")
```

```
## Warning in file(file, "rt"): cannot open file 'trump 2020 presidential election rallies.csv': No such file or directory
```

```
## Error in file(file, "rt"): cannot open the connection
```




```r
covid_us_county_level
```

```
## Error in eval(expr, envir, enclos): object 'covid_us_county_level' not found
```



```r
Tulsa<-covid_us_county_level %>% filter(Admin2=="Tulsa")
```

```
## Error in filter(., Admin2 == "Tulsa"): object 'covid_us_county_level' not found
```


```r
Maricopa<-covid_us_county_level %>% filter(Admin2=="Maricopa")
```

```
## Error in filter(., Admin2 == "Maricopa"): object 'covid_us_county_level' not found
```

```r
Blue_Earth<-covid_us_county_level %>% filter(Admin2=="Blue Earth")
```

```
## Error in filter(., Admin2 == "Blue Earth"): object 'covid_us_county_level' not found
```

```r
Winnebago<-covid_us_county_level %>% filter(Admin2=="Winnebago") %>% filter(Province_State=="Wisconsin")
```

```
## Error in filter(., Admin2 == "Winnebago"): object 'covid_us_county_level' not found
```

```r
Yuma<-covid_us_county_level %>% filter(Admin2=="Yuma") %>% filter(Province_State=="Arizona")
```

```
## Error in filter(., Admin2 == "Yuma"): object 'covid_us_county_level' not found
```

```r
Lackawanna<-covid_us_county_level %>% filter(Admin2=="Lackawanna")
```

```
## Error in filter(., Admin2 == "Lackawanna"): object 'covid_us_county_level' not found
```

```r
Rockingham<-covid_us_county_level %>% filter(Admin2=="Rockingham") %>% filter(Province_State=="New Hampshire")
```

```
## Error in filter(., Admin2 == "Rockingham"): object 'covid_us_county_level' not found
```

```r
Westmoreland<-covid_us_county_level %>% filter(Admin2=="Westmoreland") %>% filter(Province_State=="Pennsylvania")
```

```
## Error in filter(., Admin2 == "Westmoreland"): object 'covid_us_county_level' not found
```

```r
Forsyth<-covid_us_county_level %>% filter(Admin2=="Forsyth") %>% filter(Province_State=="North Carolina")
```

```
## Error in filter(., Admin2 == "Forsyth"): object 'covid_us_county_level' not found
```

```r
Saginaw<-covid_us_county_level %>% filter(Admin2=="Saginaw")
```

```
## Error in filter(., Admin2 == "Saginaw"): object 'covid_us_county_level' not found
```

```r
Clark<-covid_us_county_level %>% filter(Admin2=="Clark")%>% filter(Province_State=="Nevada")
```

```
## Error in filter(., Admin2 == "Clark"): object 'covid_us_county_level' not found
```

```r
Douglas<-covid_us_county_level %>% filter(Admin2=="Douglas")
```

```
## Error in filter(., Admin2 == "Douglas"): object 'covid_us_county_level' not found
```

```r
Marathon<-covid_us_county_level %>% filter(Admin2=="Marathon")
```

```
## Error in filter(., Admin2 == "Marathon"): object 'covid_us_county_level' not found
```

```r
Beltrami<-covid_us_county_level %>% filter(Admin2=="Beltrami")
```

```
## Error in filter(., Admin2 == "Beltrami"): object 'covid_us_county_level' not found
```

```r
Cumberland<-covid_us_county_level %>% filter(Admin2=="Cumberland") %>% filter(Province_State=="North Carolina")
```

```
## Error in filter(., Admin2 == "Cumberland"): object 'covid_us_county_level' not found
```

```r
Lucas<-covid_us_county_level %>% filter(Admin2=="Lucas") %>% filter(Province_State=="Ohio")
```

```
## Error in filter(., Admin2 == "Lucas"): object 'covid_us_county_level' not found
```

```r
Vandalia <-covid_us_county_level %>% filter(Admin2=="Vandalia")
```

```
## Error in filter(., Admin2 == "Vandalia"): object 'covid_us_county_level' not found
```

```r
Allegheny<-covid_us_county_level %>% filter(Admin2=="Allegheny")
```

```
## Error in filter(., Admin2 == "Allegheny"): object 'covid_us_county_level' not found
```

```r
Duval<-covid_us_county_level %>% filter(Admin2=="Duval") %>% filter(Province_State=="Florida")
```

```
## Error in filter(., Admin2 == "Duval"): object 'covid_us_county_level' not found
```

```r
Newport_News<-covid_us_county_level %>% filter(Admin2=="Newport News")
```

```
## Error in filter(., Admin2 == "Newport News"): object 'covid_us_county_level' not found
```

```r
Dauphin<-covid_us_county_level %>% filter(Admin2=="Dauphin")
```

```
## Error in filter(., Admin2 == "Dauphin"): object 'covid_us_county_level' not found
```


```r
Tulsa_date<-Tulsa %>% separate(Last_Update,c("date","time"),sep=" ")
```

```
## Error in separate(., Last_Update, c("date", "time"), sep = " "): object 'Tulsa' not found
```

```r
Tulsa_date$date<-as.Date(parse_date_time(Tulsa_date$date, orders = c("%m/%d/%y","%y-%m-%d")))
```

```
## Error in .num_to_date(x): object 'Tulsa_date' not found
```

```r
Tulsa_date_narrow<-Tulsa_date %>% filter(date>=as.Date("2020-04-20") & date<=as.Date("2020-07-20"))
```

```
## Error in filter(., date >= as.Date("2020-04-20") & date <= as.Date("2020-07-20")): object 'Tulsa_date' not found
```


```r
#install.packages("showtext")
library(showtext)
font_add("Arial", "/Library/Fonts/Arial.ttf")  # Use the actual file path
showtext_auto()
```



```r
library(xaringanthemer)
style_mono_accent(
  base_color = "#FF7F50",               # bright red
  inverse_background_color = "#002B36", # dark dark blue
  inverse_header_color = "#31b09e",     # light aqua green
  inverse_text_color = "#FFFFFF",       # white
  title_slide_background_color = "var(--base)",
  text_font_google = google_font("Kelly Slab"),
  header_font_google = google_font("Oleo Script")
)
```


There are no firm numbers on how long it takes to get an accurate positive test result. The time from exposure to the onset of symptoms is around two to 14 days, according to Harvard Health. Most people’s symptoms appear around day five, on average.



```r
ggplot(Tulsa_date_narrow,aes(x=date,y=Confirmed))+geom_line(col="lightsteelblue2",size =1.5,arrow =arrow())+geom_point(color="coral")+scale_x_date(date_breaks = "10 day", limits = as.Date(c("2020-04-20","2020-07-17")))+scale_y_continuous(breaks =seq(0,12000,1000))+labs(title="Covid Daily Comfirmed Cases for Tulsa, Oklahoma",caption= "Source: Novel Coronavirus (COVID-19) Cases, provided by JHU CSSE",y="Confirmed Covid Cases Per Day")+geom_vline(xintercept = as.Date("2020-06-20"), linetype = "dashed",size=0.3,col="coral")+theme_xaringan()+
  theme(plot.title = element_text(size = 16, face = "bold", hjust = 0.5), 
        axis.text.x = element_text(size=8,angle=-45, hjust=0.1,vjust=1), 
        axis.text.y = element_text(size=10, face="bold"), 
        axis.title.y = element_text(size=10,face="bold"),
        axis.title.x = element_blank(),
        plot.caption = element_text(size=11, face="bold"),
        panel.grid.major.x = element_blank()
        )
```

```
## Error in ggplot(Tulsa_date_narrow, aes(x = date, y = Confirmed)): object 'Tulsa_date_narrow' not found
```




```r
ggplot(Tulsa_date_narrow,aes(x=date,y=Confirmed))+geom_line(col="lightsteelblue2",size =1.5,arrow = arrow())+geom_point(color="coral")+scale_x_date(date_breaks = "10 day", 
                 limits = as.Date(c("2020-04-20","2020-07-17")))+scale_y_continuous(breaks =seq(0,12000,1000))+labs(title="Covid Daily Comfirmed Cases for Tulsa, Oklahoma",caption= "Source: Novel Coronavirus (COVID-19) Cases, provided by JHU CSSE",y="Confirmed Covid Cases Per Day")+geom_vline(xintercept = as.Date("2020-06-20"), linetype = "dashed",size=0.5                                              ,col="coral")+theme_xaringan()+
  theme(plot.title = element_text(size = 16, face = "bold", hjust = 0.5), 
        axis.text.x = element_text(size=8,angle=-45, hjust=0.1,vjust=1), 
        axis.text.y = element_text(size=10, face="bold"), 
        axis.title.y = element_text(size=10,face="bold"),
        axis.title.x = element_blank(),
        plot.caption = element_text(size=11, face="bold"),
        panel.grid.major.x = element_blank()
        )
```

```
## Error in ggplot(Tulsa_date_narrow, aes(x = date, y = Confirmed)): object 'Tulsa_date_narrow' not found
```

6/23/20


```r
Maricopa_date<-Maricopa %>% separate(Last_Update,c("date","time"),sep=" ")
```

```
## Error in separate(., Last_Update, c("date", "time"), sep = " "): object 'Maricopa' not found
```

```r
Maricopa_date$date<-as.Date(parse_date_time(Maricopa_date$date, orders = c("%m/%d/%y","%y-%m-%d")))
```

```
## Error in .num_to_date(x): object 'Maricopa_date' not found
```

```r
Maricopa_date_narrow<-Maricopa_date %>% filter(date>=as.Date("2020-04-23") & date<=as.Date("2020-07-23"))
```

```
## Error in filter(., date >= as.Date("2020-04-23") & date <= as.Date("2020-07-23")): object 'Maricopa_date' not found
```


```r
ggplot(Maricopa_date_narrow,aes(x=date,y=Confirmed))+geom_line(col="lightsteelblue2",size =1.5,arrow = arrow())+geom_point(color="coral")+scale_x_date(date_breaks = "10 day", 
                 limits = as.Date(c("2020-04-23","2020-07-23")))+scale_y_continuous(breaks =seq(0,100000,20000))+labs(title="Covid Daily Comfirmed Cases for Maricopa(Phoenix), Arizona",caption= "Source: Novel Coronavirus (COVID-19) Cases, provided by JHU CSSE",y="Confirmed Covid Cases Per Day")+geom_vline(xintercept = as.Date("2020-06-23"), linetype = "dashed",size=0.5                                              ,col="coral")+theme_xaringan()+
  theme(plot.title = element_text(size = 16, face = "bold", hjust = 0.5), 
        axis.text.x = element_text(size=8,angle=-45, hjust=0.1,vjust=1), 
        axis.text.y = element_text(size=10, face="bold"), 
        axis.title.y = element_text(size=10,face="bold"),
        axis.title.x = element_blank(),
        plot.caption = element_text(size=11, face="bold"),
        panel.grid.major.x = element_blank()
        )
```

```
## Error in ggplot(Maricopa_date_narrow, aes(x = date, y = Confirmed)): object 'Maricopa_date_narrow' not found
```
8/17/20



```r
Blue_Earth_date<-Blue_Earth %>% separate(Last_Update,c("date","time"),sep=" ")
```

```
## Error in separate(., Last_Update, c("date", "time"), sep = " "): object 'Blue_Earth' not found
```

```r
Blue_Earth_date$date<-as.Date(parse_date_time(Blue_Earth_date$date, orders = c("%m/%d/%y","%y-%m-%d")))
```

```
## Error in .num_to_date(x): object 'Blue_Earth_date' not found
```

```r
Blue_Earth_date_narrow<-Blue_Earth_date %>% filter(date>=as.Date("2020-06-17") & date<=as.Date("2020-09-17"))
```

```
## Error in filter(., date >= as.Date("2020-06-17") & date <= as.Date("2020-09-17")): object 'Blue_Earth_date' not found
```


```r
ggplot(Blue_Earth_date_narrow,aes(x=date,y=Confirmed))+geom_line(col="lightsteelblue2",size =1.5,arrow = arrow())+geom_point(color="coral")+scale_x_date(date_breaks = "6 day", limits = as.Date(c("2020-06-17","2020-09-17")))+scale_y_continuous(breaks =seq(0,2000,200))+labs(title="Covid Daily Comfirmed Cases for Maricopa(Phoenix), Arizona",caption= "Source: Novel Coronavirus (COVID-19) Cases, provided by JHU CSSE",y="Confirmed Covid Cases Per Day")+geom_vline(xintercept = as.Date("2020-08-17"), linetype = "dashed",size=0.5                                              ,col="coral")+theme_xaringan()+
  theme(plot.title = element_text(size = 16, face = "bold", hjust = 0.5), 
        axis.text.x = element_text(size=8,angle=-45, hjust=0.1,vjust=1), 
        axis.text.y = element_text(size=10, face="bold"), 
        axis.title.y = element_text(size=10,face="bold"),
        axis.title.x = element_blank(),
        plot.caption = element_text(size=11, face="bold"),
        panel.grid.major.x = element_blank()
        
        )
```

```
## Error in ggplot(Blue_Earth_date_narrow, aes(x = date, y = Confirmed)): object 'Blue_Earth_date_narrow' not found
```


```r
Winnebago_date<-Winnebago %>% separate(Last_Update,c("date","time"),sep=" ")
```

```
## Error in separate(., Last_Update, c("date", "time"), sep = " "): object 'Winnebago' not found
```

```r
Winnebago_date$date<-as.Date(parse_date_time(Winnebago_date$date, orders = c("%m/%d/%y","%y-%m-%d")))
```

```
## Error in .num_to_date(x): object 'Winnebago_date' not found
```

```r
Winnebago_date_narrow<-Winnebago_date %>% filter(date>=as.Date("2020-06-17") & date<=as.Date("2020-09-17"))
```

```
## Error in filter(., date >= as.Date("2020-06-17") & date <= as.Date("2020-09-17")): object 'Winnebago_date' not found
```


```r
ggplot(Winnebago_date_narrow,aes(x=date,y=Confirmed))+geom_line(col="lightsteelblue2",size =1.5,arrow = arrow())+geom_point(color="coral")+scale_x_date(date_breaks = "10 day", limits = as.Date(c("2020-06-17","2020-09-17")))+scale_y_continuous(breaks =seq(0,20000,200))+labs(title="Covid Daily Comfirmed Cases for Maricopa(Phoenix), Arizona",caption= "Source: Novel Coronavirus (COVID-19) Cases, provided by JHU CSSE",y="Confirmed Covid Cases Per Day")+geom_vline(xintercept = as.Date("2020-08-17"), linetype = "dashed",size=0.5                                              ,col="coral")+theme_xaringan()+
  theme(plot.title = element_text(size = 16, face = "bold", hjust = 0.5), 
        axis.text.x = element_text(size=8,angle=-45, hjust=0.1,vjust=1), 
        axis.text.y = element_text(size=10, face="bold"), 
        axis.title.y = element_text(size=10,face="bold"),
        axis.title.x = element_blank(),
        plot.caption = element_text(size=11, face="bold"),
        panel.grid.major.x = element_blank()
        )
```

```
## Error in ggplot(Winnebago_date_narrow, aes(x = date, y = Confirmed)): object 'Winnebago_date_narrow' not found
```
8/18/20


```r
Yuma_date<-Yuma%>% separate(Last_Update,c("date","time"),sep=" ")
```

```
## Error in separate(., Last_Update, c("date", "time"), sep = " "): object 'Yuma' not found
```

```r
Yuma_date$date<-as.Date(parse_date_time(Yuma_date$date, orders = c("%m/%d/%y","%y-%m-%d")))
```

```
## Error in .num_to_date(x): object 'Yuma_date' not found
```

```r
Yuma_date_narrow<-Yuma_date %>% filter(date>=as.Date("2020-06-18") & date<=as.Date("2020-09-18"))
```

```
## Error in filter(., date >= as.Date("2020-06-18") & date <= as.Date("2020-09-18")): object 'Yuma_date' not found
```


```r
ggplot(Yuma_date_narrow,aes(x=date,y=Confirmed))+geom_line(col="lightsteelblue2",size =1.5,arrow = arrow())+geom_point(color="coral")+scale_x_date(date_breaks = "10 day", 
                 limits = as.Date(c("2020-06-18","2020-09-18")))+scale_y_continuous(breaks =seq(0,20000,2000))+labs(title="Covid Daily Comfirmed Cases for Maricopa(Phoenix), Arizona",caption= "Source: Novel Coronavirus (COVID-19) Cases, provided by JHU CSSE",y="Confirmed Covid Cases Per Day")+geom_vline(xintercept = as.Date("2020-08-18"), linetype = "dashed",size=0.5                                              ,col="coral")+theme_xaringan()+
  theme(plot.title = element_text(size = 16, face = "bold", hjust = 0.5), 
        axis.text.x = element_text(size=8,angle=-45, hjust=0.1,vjust=1), 
        axis.text.y = element_text(size=10, face="bold"), 
        axis.title.y = element_text(size=10,face="bold"),
        axis.title.x = element_blank(),
        plot.caption = element_text(size=11, face="bold"),
        panel.grid.major.x = element_blank()
        )
```

```
## Error in ggplot(Yuma_date_narrow, aes(x = date, y = Confirmed)): object 'Yuma_date_narrow' not found
```
8/20/20

```r
Lackawanna_date<-Lackawanna%>% separate(Last_Update,c("date","time"),sep=" ")
```

```
## Error in separate(., Last_Update, c("date", "time"), sep = " "): object 'Lackawanna' not found
```

```r
Lackawanna_date$date<-as.Date(parse_date_time(Lackawanna_date$date, orders = c("%m/%d/%y","%y-%m-%d")))
```

```
## Error in .num_to_date(x): object 'Lackawanna_date' not found
```

```r
Lackawanna_date_narrow<-Lackawanna_date %>% filter(date>=as.Date("2020-06-20") & date<=as.Date("2020-09-20"))
```

```
## Error in filter(., date >= as.Date("2020-06-20") & date <= as.Date("2020-09-20")): object 'Lackawanna_date' not found
```

```r
ggplot(Lackawanna_date_narrow,aes(x=date,y=Confirmed))+geom_line(col="lightsteelblue2",size =1.5,arrow = arrow())+geom_point(color="coral")+scale_x_date(date_breaks = "10 day", 
                 limits = as.Date(c("2020-06-20","2020-09-20")))+scale_y_continuous(breaks =seq(1600,4000,200))+labs(title="Covid Daily Comfirmed Cases for Maricopa(Phoenix), Arizona",caption= "Source: Novel Coronavirus (COVID-19) Cases, provided by JHU CSSE",y="Confirmed Covid Cases Per Day")+geom_vline(xintercept = as.Date("2020-08-20"), linetype = "dashed",size=0.5                                              ,col="coral")+theme_xaringan()+
  theme(plot.title = element_text(size = 16, face = "bold", hjust = 0.5), 
        axis.text.x = element_text(size=8,angle=-45, hjust=0.1,vjust=1), 
        axis.text.y = element_text(size=10, face="bold"), 
        axis.title.y = element_text(size=10,face="bold"),
        axis.title.x = element_blank(),
        plot.caption = element_text(size=11, face="bold"),
        panel.grid.major.x = element_blank()
        )
```

```
## Error in ggplot(Lackawanna_date_narrow, aes(x = date, y = Confirmed)): object 'Lackawanna_date_narrow' not found
```
8/28/20


```r
Rockingham_date<-Rockingham%>% separate(Last_Update,c("date","time"),sep=" ")
```

```
## Error in separate(., Last_Update, c("date", "time"), sep = " "): object 'Rockingham' not found
```

```r
Rockingham_date$date<-as.Date(parse_date_time(Rockingham_date$date, orders = c("%m/%d/%y","%y-%m-%d")))
```

```
## Error in .num_to_date(x): object 'Rockingham_date' not found
```

```r
Rockingham_date_narrow<-Rockingham_date %>% filter(date>=as.Date("2020-06-28") & date<=as.Date("2020-09-28"))
```

```
## Error in filter(., date >= as.Date("2020-06-28") & date <= as.Date("2020-09-28")): object 'Rockingham_date' not found
```


```r
ggplot(Rockingham_date_narrow,aes(x=date,y=Confirmed))+geom_line(col="lightsteelblue2",size =1.5,arrow = arrow())+geom_point(color="coral")+scale_x_date(date_breaks = "10 day", 
                 limits = as.Date(c("2020-06-28","2020-09-28")))+scale_y_continuous(breaks =seq(1600,4000,200))+labs(title="Covid Daily Comfirmed Cases for Maricopa(Phoenix), Arizona",caption= "Source: Novel Coronavirus (COVID-19) Cases, provided by JHU CSSE",y="Confirmed Covid Cases Per Day")+geom_vline(xintercept = as.Date("2020-08-28"), linetype = "dashed",size=0.5                                              ,col="coral")+theme_xaringan()+
  theme(plot.title = element_text(size = 16, face = "bold", hjust = 0.5), 
        axis.text.x = element_text(size=8,angle=-45, hjust=0.1,vjust=1), 
        axis.text.y = element_text(size=10, face="bold"), 
        axis.title.y = element_text(size=10,face="bold"),
        axis.title.x = element_blank(),
        plot.caption = element_text(size=11, face="bold"),
        panel.grid.major.x = element_blank()
        )
```

```
## Error in ggplot(Rockingham_date_narrow, aes(x = date, y = Confirmed)): object 'Rockingham_date_narrow' not found
```
9/3/20

```r
Westmoreland_date<-Westmoreland%>% separate(Last_Update,c("date","time"),sep=" ")
```

```
## Error in separate(., Last_Update, c("date", "time"), sep = " "): object 'Westmoreland' not found
```

```r
Westmoreland_date$date<-as.Date(parse_date_time(Westmoreland_date$date, orders = c("%m/%d/%y","%y-%m-%d")))
```

```
## Error in .num_to_date(x): object 'Westmoreland_date' not found
```

```r
Westmoreland_date_narrow<-Westmoreland_date %>% filter(date>=as.Date("2020-07-03") & date<=as.Date("2020-10-03"))
```

```
## Error in filter(., date >= as.Date("2020-07-03") & date <= as.Date("2020-10-03")): object 'Westmoreland_date' not found
```


```r
ggplot(Westmoreland_date_narrow,aes(x=date,y=Confirmed))+geom_line(col="lightsteelblue2",size =1.5,arrow = arrow())+geom_point(color="coral")+scale_x_date(date_breaks = "10 day", 
                 limits = as.Date(c("2020-06-28","2020-09-28")))+scale_y_continuous(breaks =seq(0,4000,200))+labs(title="Covid Daily Comfirmed Cases for Maricopa(Phoenix), Arizona",caption= "Source: Novel Coronavirus (COVID-19) Cases, provided by JHU CSSE",y="Confirmed Covid Cases Per Day")+geom_vline(xintercept = as.Date("2020-09-03"), linetype = "dashed",size=0.5                                              ,col="coral")+theme_xaringan()+
  theme(plot.title = element_text(size = 16, face = "bold", hjust = 0.5), 
        axis.text.x = element_text(size=8,angle=-45, hjust=0.1,vjust=1), 
        axis.text.y = element_text(size=10, face="bold"), 
        axis.title.y = element_text(size=10,face="bold"),
        axis.title.x = element_blank(),
        plot.caption = element_text(size=11, face="bold"),
        panel.grid.major.x = element_blank()
        )
```

```
## Error in ggplot(Westmoreland_date_narrow, aes(x = date, y = Confirmed)): object 'Westmoreland_date_narrow' not found
```
9/8/20

```r
Forsyth_date<-Forsyth%>% separate(Last_Update,c("date","time"),sep=" ")
```

```
## Error in separate(., Last_Update, c("date", "time"), sep = " "): object 'Forsyth' not found
```

```r
Forsyth_date$date<-as.Date(parse_date_time(Forsyth_date$date, orders = c("%m/%d/%y","%y-%m-%d")))
```

```
## Error in .num_to_date(x): object 'Forsyth_date' not found
```

```r
Forsyth_date_narrow<-Forsyth_date %>% filter(date>=as.Date("2020-07-08") & date<=as.Date("2020-10-08"))
```

```
## Error in filter(., date >= as.Date("2020-07-08") & date <= as.Date("2020-10-08")): object 'Forsyth_date' not found
```


```r
ggplot(Forsyth_date_narrow,aes(x=date,y=Confirmed))+geom_line(col="lightsteelblue2",size =1.5,arrow = arrow())+geom_point(color="coral")+scale_x_date(date_breaks = "10 day", 
                 limits = as.Date(c("2020-07-08","2020-10-08")))+scale_y_continuous(breaks =seq(2000,20000,1000))+labs(title="Covid Daily Comfirmed Cases for Maricopa(Phoenix), Arizona",caption= "Source: Novel Coronavirus (COVID-19) Cases, provided by JHU CSSE",y="Confirmed Covid Cases Per Day")+geom_vline(xintercept = as.Date("2020-09-08"), linetype = "dashed",size=0.5                                              ,col="coral")+theme_xaringan()+
  theme(plot.title = element_text(size = 16, face = "bold", hjust = 0.5), 
        axis.text.x = element_text(size=8,angle=-45, hjust=0.1,vjust=1), 
        axis.text.y = element_text(size=10, face="bold"), 
        axis.title.y = element_text(size=10,face="bold"),
        axis.title.x = element_blank(),
        plot.caption = element_text(size=11, face="bold"),
        panel.grid.major.x = element_blank()
        )
```

```
## Error in ggplot(Forsyth_date_narrow, aes(x = date, y = Confirmed)): object 'Forsyth_date_narrow' not found
```
9/10/20


```r
Saginaw_date<-Forsyth%>% separate(Last_Update,c("date","time"),sep=" ")
```

```
## Error in separate(., Last_Update, c("date", "time"), sep = " "): object 'Forsyth' not found
```

```r
Saginaw_date$date<-as.Date(parse_date_time(Saginaw_date$date, orders = c("%m/%d/%y","%y-%m-%d")))
```

```
## Error in .num_to_date(x): object 'Saginaw_date' not found
```

```r
Saginaw_date_narrow<-Saginaw_date %>% filter(date>=as.Date("2020-07-10") & date<=as.Date("2020-10-10"))
```

```
## Error in filter(., date >= as.Date("2020-07-10") & date <= as.Date("2020-10-10")): object 'Saginaw_date' not found
```


```r
ggplot(Saginaw_date_narrow,aes(x=date,y=Confirmed))+geom_line(col="lightsteelblue2",size =1.5,arrow = arrow())+geom_point(color="coral")+scale_x_date(date_breaks = "10 day", 
                 limits = as.Date(c("2020-07-10","2020-10-10")))+scale_y_continuous(breaks =seq(2000,20000,1000))+labs(title="Covid Daily Comfirmed Cases for Maricopa(Phoenix), Arizona",caption= "Source: Novel Coronavirus (COVID-19) Cases, provided by JHU CSSE",y="Confirmed Covid Cases Per Day")+geom_vline(xintercept = as.Date("2020-09-10"), linetype = "dashed",size=0.5                                              ,col="coral")+theme_xaringan()+
  theme(plot.title = element_text(size = 16, face = "bold", hjust = 0.5), 
        axis.text.x = element_text(size=8,angle=-45, hjust=0.1,vjust=1), 
        axis.text.y = element_text(size=10, face="bold"), 
        axis.title.y = element_text(size=10,face="bold"),
        axis.title.x = element_blank(),
        plot.caption = element_text(size=11, face="bold"),
        panel.grid.major.x = element_blank()
        )
```

```
## Error in ggplot(Saginaw_date_narrow, aes(x = date, y = Confirmed)): object 'Saginaw_date_narrow' not found
```
9/12/20

```r
Douglas_date<-Forsyth%>% separate(Last_Update,c("date","time"),sep=" ")
```

```
## Error in separate(., Last_Update, c("date", "time"), sep = " "): object 'Forsyth' not found
```

```r
Douglas_date$date<-as.Date(parse_date_time(Douglas_date$date, orders = c("%m/%d/%y","%y-%m-%d")))
```

```
## Error in .num_to_date(x): object 'Douglas_date' not found
```

```r
Douglas_date_narrow<-Douglas_date %>% filter(date>=as.Date("2020-07-12") & date<=as.Date("2020-10-12"))
```

```
## Error in filter(., date >= as.Date("2020-07-12") & date <= as.Date("2020-10-12")): object 'Douglas_date' not found
```


```r
ggplot(Douglas_date_narrow,aes(x=date,y=Confirmed))+geom_line(col="lightsteelblue2",size =1.5,arrow = arrow())+geom_point(color="coral")+scale_x_date(date_breaks = "10 day", 
                 limits = as.Date(c("2020-07-10","2020-10-10")))+scale_y_continuous(breaks =seq(2000,20000,1000))+labs(title="Covid Daily Comfirmed Cases for Maricopa(Phoenix), Arizona",caption= "Source: Novel Coronavirus (COVID-19) Cases, provided by JHU CSSE",y="Confirmed Covid Cases Per Day")+geom_vline(xintercept = as.Date("2020-09-10"), linetype = "dashed",size=0.5                                              ,col="coral")+theme_xaringan()+
  theme(plot.title = element_text(size = 16, face = "bold", hjust = 0.5), 
        axis.text.x = element_text(size=8,angle=-45, hjust=0.1,vjust=1), 
        axis.text.y = element_text(size=10, face="bold"), 
        axis.title.y = element_text(size=10,face="bold"),
        axis.title.x = element_blank(),
        plot.caption = element_text(size=11, face="bold"),
        panel.grid.major.x = element_blank()
        )
```

```
## Error in ggplot(Douglas_date_narrow, aes(x = date, y = Confirmed)): object 'Douglas_date_narrow' not found
```
9/13/20


```r
rect <- data.frame(xmin=as.Date("2020-09-08"), xmax=as.Date("2020-09-15"), ymin=-Inf, ymax=Inf)
```




```r
Clark_date<-Clark%>% separate(Last_Update,c("date","time"),sep=" ")
```

```
## Error in separate(., Last_Update, c("date", "time"), sep = " "): object 'Clark' not found
```

```r
Clark_date$date<-as.Date(parse_date_time(Clark_date$date, orders = c("%m/%d/%y","%y-%m-%d")))
```

```
## Error in .num_to_date(x): object 'Clark_date' not found
```

```r
Clark_date_narrow<-Clark_date %>% filter(date>=as.Date("2020-08-13") & date<=as.Date("2020-10-03"))
```

```
## Error in filter(., date >= as.Date("2020-08-13") & date <= as.Date("2020-10-03")): object 'Clark_date' not found
```


```r
Clark_date_narrow
```

```
## Error in eval(expr, envir, enclos): object 'Clark_date_narrow' not found
```





```r
ggplot(Clark_date_narrow,aes(x=date,y=Confirmed))+geom_rect(data=rect, aes(xmin=xmin, xmax=xmax, ymin=ymin, ymax=ymax),
              fill="lightyellow",
              alpha=0.5,
              inherit.aes = FALSE)+geom_line(col="lightsteelblue2",size =1.5,arrow = arrow())+geom_point(color="coral")+scale_x_date(date_breaks = "7 day", 
                 limits = as.Date(c("2020-08-13","2020-10-03")))+scale_y_continuous(breaks =seq(2000,20000,1000))+labs(title="Covid Daily Comfirmed Cases for Maricopa(Phoenix), Arizona",caption= "Source: Novel Coronavirus (COVID-19) Cases, provided by JHU CSSE",y="Confirmed Covid Cases Per Day")+geom_vline(xintercept = as.Date("2020-09-13"), linetype = "dashed",size=0.5,col="coral")+theme_xaringan()+
  theme(plot.title = element_text(size = 16, face = "bold", hjust = 0.5), 
        axis.text.x = element_text(size=8,angle=-45, hjust=0.1,vjust=1), 
        axis.text.y = element_text(size=10, face="bold"), 
        axis.title.y = element_text(size=10,face="bold"),
        axis.title.x = element_blank(),
        plot.caption = element_text(size=11, face="bold"),
        panel.grid.major.x = element_blank()
        )
```

```
## Error in ggplot(Clark_date_narrow, aes(x = date, y = Confirmed)): object 'Clark_date_narrow' not found
```
9/17/20

```r
Marathon_date<-Marathon%>% separate(Last_Update,c("date","time"),sep=" ")
```

```
## Error in separate(., Last_Update, c("date", "time"), sep = " "): object 'Marathon' not found
```

```r
Marathon_date$date<-as.Date(parse_date_time(Marathon_date$date, orders = c("%m/%d/%y","%y-%m-%d")))
```

```
## Error in .num_to_date(x): object 'Marathon_date' not found
```

```r
Marathon_date_narrow<-Marathon_date %>% filter(date>=as.Date("2020-08-17") & date<=as.Date("2020-10-17"))
```

```
## Error in filter(., date >= as.Date("2020-08-17") & date <= as.Date("2020-10-17")): object 'Marathon_date' not found
```


```r
ggplot(Marathon_date_narrow,aes(x=date,y=Confirmed))+geom_line(col="lightsteelblue2",size =1.5,arrow = arrow())+geom_point(color="coral")+scale_x_date(date_breaks = "7 day", 
                 limits = as.Date(c("2020-08-13","2020-10-03")))+scale_y_continuous(breaks =seq(0,5000,500))+labs(title="Covid Daily Comfirmed Cases for Maricopa(Phoenix), Arizona",caption= "Source: Novel Coronavirus (COVID-19) Cases, provided by JHU CSSE",y="Confirmed Covid Cases Per Day")+geom_vline(xintercept = as.Date("2020-09-17"), linetype = "dashed",size=0.5,col="coral")+theme_xaringan()+
  theme(plot.title = element_text(size = 16, face = "bold", hjust = 0.5), 
        axis.text.x = element_text(size=8,angle=-45, hjust=0.1,vjust=1), 
        axis.text.y = element_text(size=10, face="bold"), 
        axis.title.y = element_text(size=10,face="bold"),
        axis.title.x = element_blank(),
        plot.caption = element_text(size=11, face="bold"),
        panel.grid.major.x = element_blank()
        )
```

```
## Error in ggplot(Marathon_date_narrow, aes(x = date, y = Confirmed)): object 'Marathon_date_narrow' not found
```
9/18/20

```r
Beltrami_date<-Beltrami%>% separate(Last_Update,c("date","time"),sep=" ")
```

```
## Error in separate(., Last_Update, c("date", "time"), sep = " "): object 'Beltrami' not found
```

```r
Beltrami_date$date<-as.Date(parse_date_time(Beltrami_date$date, orders = c("%m/%d/%y","%y-%m-%d")))
```

```
## Error in .num_to_date(x): object 'Beltrami_date' not found
```

```r
Beltrami_date_narrow<-Beltrami_date %>% filter(date>=as.Date("2020-08-18") & date<=as.Date("2020-10-18"))
```

```
## Error in filter(., date >= as.Date("2020-08-18") & date <= as.Date("2020-10-18")): object 'Beltrami_date' not found
```


```r
ggplot(Beltrami_date_narrow,aes(x=date,y=Confirmed))+geom_line(col="lightsteelblue2",size =1.5,arrow = arrow())+geom_point(color="coral")+scale_x_date(date_breaks = "7 day", 
                 limits = as.Date(c("2020-08-18","2020-10-18")))+scale_y_continuous(breaks =seq(0,5000,500))+labs(title="Covid Daily Comfirmed Cases for Maricopa(Phoenix), Arizona",caption= "Source: Novel Coronavirus (COVID-19) Cases, provided by JHU CSSE",y="Confirmed Covid Cases Per Day")+geom_vline(xintercept = as.Date("2020-09-18"), linetype = "dashed",size=0.5,col="coral")+theme_xaringan()+
  theme(plot.title = element_text(size = 16, face = "bold", hjust = 0.5), 
        axis.text.x = element_text(size=8,angle=-45, hjust=0.1,vjust=1), 
        axis.text.y = element_text(size=10, face="bold"), 
        axis.title.y = element_text(size=10,face="bold"),
        axis.title.x = element_blank(),
        plot.caption = element_text(size=11, face="bold"),
        panel.grid.major.x = element_blank()
        )
```

```
## Error in ggplot(Beltrami_date_narrow, aes(x = date, y = Confirmed)): object 'Beltrami_date_narrow' not found
```
9/19/20


```r
Cumberland_date<-Cumberland%>% separate(Last_Update,c("date","time"),sep=" ")
```

```
## Error in separate(., Last_Update, c("date", "time"), sep = " "): object 'Cumberland' not found
```

```r
Cumberland_date$date<-as.Date(parse_date_time(Cumberland_date$date, orders = c("%m/%d/%y","%y-%m-%d")))
```

```
## Error in .num_to_date(x): object 'Cumberland_date' not found
```

```r
Cumberland_date_narrow<-Cumberland_date %>% filter(date>=as.Date("2020-08-19") & date<=as.Date("2020-10-19"))
```

```
## Error in filter(., date >= as.Date("2020-08-19") & date <= as.Date("2020-10-19")): object 'Cumberland_date' not found
```


```r
ggplot(Cumberland_date_narrow,aes(x=date,y=Confirmed))+geom_line(col="lightsteelblue2",size =1.5,arrow = arrow())+geom_point(color="coral")+scale_x_date(date_breaks = "7 day", 
                 limits = as.Date(c("2020-08-19","2020-10-19")))+scale_y_continuous(breaks =seq(0,5000,500))+labs(title="Covid Daily Comfirmed Cases for Maricopa(Phoenix), Arizona",caption= "Source: Novel Coronavirus (COVID-19) Cases, provided by JHU CSSE",y="Confirmed Covid Cases Per Day")+geom_vline(xintercept = as.Date("2020-09-19"), linetype = "dashed",size=0.5,col="coral")+theme_xaringan()+
  theme(plot.title = element_text(size = 16, face = "bold", hjust = 0.5), 
        axis.text.x = element_text(size=8,angle=-45, hjust=0.1,vjust=1), 
        axis.text.y = element_text(size=10, face="bold"), 
        axis.title.y = element_text(size=10,face="bold"),
        axis.title.x = element_blank(),
        plot.caption = element_text(size=11, face="bold"),
        panel.grid.major.x = element_blank()
        )
```

```
## Error in ggplot(Cumberland_date_narrow, aes(x = date, y = Confirmed)): object 'Cumberland_date_narrow' not found
```
9/21/2020

```r
Lucas_date<-Lucas%>% separate(Last_Update,c("date","time"),sep=" ")
```

```
## Error in separate(., Last_Update, c("date", "time"), sep = " "): object 'Lucas' not found
```

```r
Lucas_date$date<-as.Date(parse_date_time(Lucas_date$date, orders = c("%m/%d/%y","%y-%m-%d")))
```

```
## Error in .num_to_date(x): object 'Lucas_date' not found
```

```r
Lucas_date_narrow<-Lucas_date %>% filter(date>=as.Date("2020-08-21") & date<=as.Date("2020-10-21"))
```

```
## Error in filter(., date >= as.Date("2020-08-21") & date <= as.Date("2020-10-21")): object 'Lucas_date' not found
```


```r
ggplot(Lucas_date_narrow,aes(x=date,y=Confirmed))+geom_line(col="lightsteelblue2",size =1.5,arrow = arrow())+geom_point(color="coral")+scale_x_date(date_breaks = "7 day", 
                 limits = as.Date(c("2020-08-21","2020-10-21")))+scale_y_continuous(breaks =seq(0,5000,500))+labs(title="Covid Daily Comfirmed Cases for Maricopa(Phoenix), Arizona",caption= "Source: Novel Coronavirus (COVID-19) Cases, provided by JHU CSSE",y="Confirmed Covid Cases Per Day")+geom_vline(xintercept = as.Date("2020-09-21"), linetype = "dashed",size=0.5,col="coral")+theme_xaringan()+
  theme(plot.title = element_text(size = 16, face = "bold", hjust = 0.5), 
        axis.text.x = element_text(size=8,angle=-45, hjust=0.1,vjust=1), 
        axis.text.y = element_text(size=10, face="bold"), 
        axis.title.y = element_text(size=10,face="bold"),
        axis.title.x = element_blank(),
        plot.caption = element_text(size=11, face="bold"),
        panel.grid.major.x = element_blank()
        )
```

```
## Error in ggplot(Lucas_date_narrow, aes(x = date, y = Confirmed)): object 'Lucas_date_narrow' not found
```
9/21/20


```r
Vandalia_date<-Lucas%>% separate(Last_Update,c("date","time"),sep=" ")
```

```
## Error in separate(., Last_Update, c("date", "time"), sep = " "): object 'Lucas' not found
```

```r
Vandalia_date$date<-as.Date(parse_date_time(Vandalia_date$date, orders = c("%m/%d/%y","%y-%m-%d")))
```

```
## Error in .num_to_date(x): object 'Vandalia_date' not found
```

```r
Vandalia_date_narrow<-Vandalia_date %>% filter(date>=as.Date("2020-08-21") & date<=as.Date("2020-10-21"))
```

```
## Error in filter(., date >= as.Date("2020-08-21") & date <= as.Date("2020-10-21")): object 'Vandalia_date' not found
```


```r
ggplot(Vandalia_date_narrow,aes(x=date,y=Confirmed))+geom_line(col="lightsteelblue2",size =1.5,arrow = arrow())+geom_point(color="coral")+scale_x_date(date_breaks = "7 day", 
                 limits = as.Date(c("2020-08-21","2020-10-21")))+scale_y_continuous(breaks =seq(0,5000,500))+labs(title="Covid Daily Comfirmed Cases for Maricopa(Phoenix), Arizona",caption= "Source: Novel Coronavirus (COVID-19) Cases, provided by JHU CSSE",y="Confirmed Covid Cases Per Day")+geom_vline(xintercept = as.Date("2020-09-21"), linetype = "dashed",size=0.5,col="coral")+theme_xaringan()+
  theme(plot.title = element_text(size = 16, face = "bold", hjust = 0.5), 
        axis.text.x = element_text(size=8,angle=-45, hjust=0.1,vjust=1), 
        axis.text.y = element_text(size=10, face="bold"), 
        axis.title.y = element_text(size=10,face="bold"),
        axis.title.x = element_blank(),
        plot.caption = element_text(size=11, face="bold"),
        panel.grid.major.x = element_blank()
        )
```

```
## Error in ggplot(Vandalia_date_narrow, aes(x = date, y = Confirmed)): object 'Vandalia_date_narrow' not found
```
9/22/20


```r
Allegheny_date<-Allegheny%>% separate(Last_Update,c("date","time"),sep=" ")
```

```
## Error in separate(., Last_Update, c("date", "time"), sep = " "): object 'Allegheny' not found
```

```r
Allegheny_date$date<-as.Date(parse_date_time(Allegheny_date$date, orders = c("%m/%d/%y","%y-%m-%d")))
```

```
## Error in .num_to_date(x): object 'Allegheny_date' not found
```

```r
Allegheny_date_narrow<-Allegheny_date %>% filter(date>=as.Date("2020-08-22") & date<=as.Date("2020-10-22"))
```

```
## Error in filter(., date >= as.Date("2020-08-22") & date <= as.Date("2020-10-22")): object 'Allegheny_date' not found
```


```r
ggplot(Allegheny_date_narrow,aes(x=date,y=Confirmed))+geom_line(col="lightsteelblue2",size =1.5,arrow = arrow())+geom_point(color="coral")+scale_x_date(date_breaks = "7 day", 
                 limits = as.Date(c("2020-08-22","2020-10-22")))+scale_y_continuous(breaks =seq(0,5000,500))+labs(title="Covid Daily Comfirmed Cases for Maricopa(Phoenix), Arizona",caption= "Source: Novel Coronavirus (COVID-19) Cases, provided by JHU CSSE",y="Confirmed Covid Cases Per Day")+geom_vline(xintercept = as.Date("2020-09-22"), linetype = "dashed",size=0.5,col="coral")+theme_xaringan()+
  theme(plot.title = element_text(size = 16, face = "bold", hjust = 0.5), 
        axis.text.x = element_text(size=8,angle=-45, hjust=0.1,vjust=1), 
        axis.text.y = element_text(size=10, face="bold"), 
        axis.title.y = element_text(size=10,face="bold"),
        axis.title.x = element_blank(),
        plot.caption = element_text(size=11, face="bold"),
        panel.grid.major.x = element_blank()
        )
```

```
## Error in ggplot(Allegheny_date_narrow, aes(x = date, y = Confirmed)): object 'Allegheny_date_narrow' not found
```
9/24/20

```r
Duval_date<-Duval%>% separate(Last_Update,c("date","time"),sep=" ")
```

```
## Error in separate(., Last_Update, c("date", "time"), sep = " "): object 'Duval' not found
```

```r
Duval_date$date<-as.Date(parse_date_time(Duval_date$date, orders = c("%m/%d/%y","%y-%m-%d")))
```

```
## Error in .num_to_date(x): object 'Duval_date' not found
```

```r
Duval_date_narrow<-Duval_date %>% filter(date>=as.Date("2020-08-24") & date<=as.Date("2020-10-24"))
```

```
## Error in filter(., date >= as.Date("2020-08-24") & date <= as.Date("2020-10-24")): object 'Duval_date' not found
```


```r
ggplot(Duval_date_narrow,aes(x=date,y=Confirmed))+geom_line(col="lightsteelblue2",size =1.5,arrow = arrow())+geom_point(color="coral")+scale_x_date(date_breaks = "7 day", 
                 limits = as.Date(c("2020-08-24","2020-10-24")))+scale_y_continuous(breaks =seq(0,5000,500))+labs(title="Covid Daily Comfirmed Cases for Maricopa(Phoenix), Arizona",caption= "Source: Novel Coronavirus (COVID-19) Cases, provided by JHU CSSE",y="Confirmed Covid Cases Per Day")+geom_vline(xintercept = as.Date("2020-09-24"), linetype = "dashed",size=0.5,col="coral")+theme_xaringan()+
  theme(plot.title = element_text(size = 16, face = "bold", hjust = 0.5), 
        axis.text.x = element_text(size=8,angle=-45, hjust=0.1,vjust=1), 
        axis.text.y = element_text(size=10, face="bold"), 
        axis.title.y = element_text(size=10,face="bold"),
        axis.title.x = element_blank(),
        plot.caption = element_text(size=11, face="bold"),
        panel.grid.major.x = element_blank()
        )
```

```
## Error in ggplot(Duval_date_narrow, aes(x = date, y = Confirmed)): object 'Duval_date_narrow' not found
```
9/25/20


```r
Newport_News_date<-Newport_News%>% separate(Last_Update,c("date","time"),sep=" ")
```

```
## Error in separate(., Last_Update, c("date", "time"), sep = " "): object 'Newport_News' not found
```

```r
Newport_News_date$date<-as.Date(parse_date_time(Newport_News_date$date, orders = c("%m/%d/%y","%y-%m-%d")))
```

```
## Error in .num_to_date(x): object 'Newport_News_date' not found
```

```r
Newport_News_date_narrow<-Newport_News_date %>% filter(date>=as.Date("2020-08-25") & date<=as.Date("2020-10-25"))
```

```
## Error in filter(., date >= as.Date("2020-08-25") & date <= as.Date("2020-10-25")): object 'Newport_News_date' not found
```


```r
ggplot(Newport_News_date_narrow,aes(x=date,y=Confirmed))+geom_line(col="lightsteelblue2",size =1.5,arrow = arrow())+geom_point(color="coral")+scale_x_date(date_breaks = "7 day", 
                 limits = as.Date(c("2020-08-25","2020-10-25")))+scale_y_continuous(breaks =seq(0,5000,500))+labs(title="Covid Daily Comfirmed Cases for Maricopa(Phoenix), Arizona",caption= "Source: Novel Coronavirus (COVID-19) Cases, provided by JHU CSSE",y="Confirmed Covid Cases Per Day")+geom_vline(xintercept = as.Date("2020-09-25"), linetype = "dashed",size=0.5,col="coral")+theme_xaringan()+
  theme(plot.title = element_text(size = 16, face = "bold", hjust = 0.5), 
        axis.text.x = element_text(size=8,angle=-45, hjust=0.1,vjust=1), 
        axis.text.y = element_text(size=10, face="bold"), 
        axis.title.y = element_text(size=10,face="bold"),
        axis.title.x = element_blank(),
        plot.caption = element_text(size=11, face="bold"),
        panel.grid.major.x = element_blank()
        )
```

```
## Error in ggplot(Newport_News_date_narrow, aes(x = date, y = Confirmed)): object 'Newport_News_date_narrow' not found
```
9/26/20

```r
Dauphin_date<-Dauphin%>% separate(Last_Update,c("date","time"),sep=" ")
```

```
## Error in separate(., Last_Update, c("date", "time"), sep = " "): object 'Dauphin' not found
```

```r
Dauphin_date$date<-as.Date(parse_date_time(Dauphin_date$date, orders = c("%m/%d/%y","%y-%m-%d")))
```

```
## Error in .num_to_date(x): object 'Dauphin_date' not found
```

```r
Dauphin_date_narrow<-Dauphin_date %>% filter(date>=as.Date("2020-08-26") & date<=as.Date("2020-10-26"))
```

```
## Error in filter(., date >= as.Date("2020-08-26") & date <= as.Date("2020-10-26")): object 'Dauphin_date' not found
```


```r
ggplot(Dauphin_date_narrow,aes(x=date,y=Confirmed))+geom_line(col="lightsteelblue2",size =1.5,arrow = arrow())+geom_point(color="coral")+scale_x_date(date_breaks = "7 day", 
                 limits = as.Date(c("2020-08-26","2020-10-26")))+scale_y_continuous(breaks =seq(0,5000,500))+labs(title="Covid Daily Comfirmed Cases for Maricopa(Phoenix), Arizona",caption= "Source: Novel Coronavirus (COVID-19) Cases, provided by JHU CSSE",y="Confirmed Covid Cases Per Day")+geom_vline(xintercept = as.Date("2020-09-26"), linetype = "dashed",size=0.5,col="coral")+theme_xaringan()+
  theme(plot.title = element_text(size = 16, face = "bold", hjust = 0.5), 
        axis.text.x = element_text(size=8,angle=-45, hjust=0.1,vjust=1), 
        axis.text.y = element_text(size=10, face="bold"), 
        axis.title.y = element_text(size=10,face="bold"),
        axis.title.x = element_blank(),
        plot.caption = element_text(size=11, face="bold"),
        panel.grid.major.x = element_blank()
        )
```

```
## Error in ggplot(Dauphin_date_narrow, aes(x = date, y = Confirmed)): object 'Dauphin_date_narrow' not found
```

