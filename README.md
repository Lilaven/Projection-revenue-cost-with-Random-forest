# Projection revenue and cost with Random forest

The data from gen based on some belows assumptions:

First table : date, total_application, status_application (rejected , success , cancel , pending ), potential_revenue (only for succesfull application), services (let’s say there is N different services)

Second table : services, cost_to_run_services, max_increment_for_services_in_next_quartal.


•	The column ‘diff_next_event’ is added to table 1, this column describes the difference in day from the date and the upcoming holiday of the country, the cyclicity in the volumn sales of corresponding period of time implies that the distance to upcoming holidays affects sales volumn.

•	cost_to_run_services (IDR) is cost per application, which varies by the total number of applications in day as table below.
Level	Range	Cost per app

Level 1:	<= 100 :200 + k1
Level 2:	100 - <= 500:	160 + k2
Level 3:	>500:	100 + k3

k1, k2, k3 is random value from 0 to 10.


Problem:
Estimate revenue and cost model to perform a maximum profit in next quartal
