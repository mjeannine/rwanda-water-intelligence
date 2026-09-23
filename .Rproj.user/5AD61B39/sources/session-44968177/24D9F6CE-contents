library(tidyverse)

customers <- read.csv("data/raw/dim_customers.csv")

billing <- read.csv("data/raw/fact_consumption_billing.csv")

geography <- read.csv("data/raw/dim_geography.csv")

# Joining my tables
billing_full <- billing %>% left_join(customers, by = "Customer_ID")


str(billing_full)
nrow(billing_full)

consumption_by_district <- billing_full %>% group_by(District) %>% summarise(total_consumption = sum(Consumption_m3, na.rm = TRUE))
consumption_by_district



ggplot(consumption_by_district, aes(x = District, y = total_consumption)) +
  geom_col(fill = "steelblue") +
  labs(title = "Total Water Consumption by District", y = "Total Consumption (m3)")
