# Pewlett-Hackard-Analysis

## Overview of the Pewlett-Hackard-Analysis
The purpose of this analysis is to provide information regarding employees that are close to retirement. This is important to provide an overview of staffing needs and hiring plans. This is required to prevent employee shortage which can cause remaining employees to become overwhelmed with short-staffed situations. The variables used are hired date vs. birthdate to retrieve the data showing who is going to retire soon according to age. 

### Results
1. At first glance, with our first query, it looked like we had a whole lot of employees retiring. 133,776 to be exact. The problem was duplicates. 
Here we can see one employee (Sumant, Peac) listed on three rows, so this number is not accurate. 
![image](https://user-images.githubusercontent.com/30300621/181676368-d4ac46eb-668f-456b-b75b-7526e5ebaea5.png)

2. The next step was to remove the duplicates to provide a count on how many unique titles we have by employee number. This gaves us a count of 90,398 with unique titles and not duplicates. 

SELECT DISTINCT ON (emp_no) emp_no,
	first_name,
	last_name,
	title
INTO unique_titles
FROM retirement_titles
ORDER BY emp_no, title DESC;
![image](https://user-images.githubusercontent.com/30300621/181676915-7cb9c21a-fb58-4088-b788-03b9c3bd7ce9.png)

3. The next item was to count the number of employees about to retire by their most recent job title. 

![image](https://user-images.githubusercontent.com/30300621/181677438-8b2fb2a5-15ba-461d-a690-9be482b23035.png)

4. To prepare for the "silver tsunami" that is coming to Pewlett-Hackard, a Mentorship Program was established to see how many qualified candidates can be considered to mentor the next generation. This resulted in 1940 employees ready to retire that may be eligible to mentor the next generation. 

![image](https://user-images.githubusercontent.com/30300621/181677895-736b9999-0460-4cfd-b696-771c2959cbe4.png)

## Summary
This analysis shows Pewlett-Hackard needs to prepare for a huge hiring event. There will need to be several training sessions for large groups in different job categories to fill the gaps coming when the retirements begin. If 90,380 employees are preparing for retirement and there are only 1940 qualified candidates for the mentorship program. It will take each mentor to train at least 47 new hires. This is an overwhelmingly large number for one person. There is also the question on how many future retirees are willing to mentor. 

Reevaluating the mentorship program mey be the next step to increase the number of qualified candidates. This will help balance the ratio between retirees and new hires. 

