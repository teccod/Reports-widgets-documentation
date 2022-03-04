# Dimensions
### SystemVersionNumber - shows for which particular version of IRIS the application was installed.

### Name - shows the name of the application.

### TopName - stores the names of the 10 most popular applications. All other applications are designated under the name ZPM.

### Country - shows in which country the installation was made.

# Measures
### m_Count_sum - stores the total number of installs.

### m_Name distinct - stores the total number of applications for which there were installations.

### m_IP_distinct - stores the total number of IP addresses on which applications were installed.




# List 1
_On this page we have all data about activity at last month._

## Total installs

_Amount of total installs of IRIS applications._

Label displaying the parameter based on m_Count_sum from which the last month’s data is selected. At the bottom of the label there is a label with data for the last 2 month. It displays a formula for displaying the name of the month and the parameter. The parameter is a copy of the one described above, but for a different period of time. 

## Total modules

_Amount of distinct apps that have been installed._

Label displaying the parameter based on m_Name_distinct  from which the last month’s data is selected. At the bottom of the label there is a label with data for the last 2 month. It displays a formula for displaying the name of the month and the parameter. The parameter is a copy of the one described above, but for a different period of time. 

## Total hosts

_Amount of distinct ip addresses from which apps were installed._

Label displaying the parameter based on m_IP_distinct from which the last month’s data is selected. At the bottom of the label there is a label with data for the last 2 month. It displays a formula for displaying the name of the month and the parameter. The parameter is a copy of the one described above, but for a different period of time. 

## MTM formulas and YTY formulas

	number percent;
	number @now = parameter displayed above formula.
	number @last = parameter similar to displayed above formula but for last 2 months or last year
	//In all formulas, parameters are used directly in the formula, without additional assignment to variables. This assignment is shown to understand how the formula works.
	percent = (@now - @last) / @last *100;
	if (percent > 0) 
		{return '↑ '+ ToText(Truncate(percent,1))+ ' % MTM';}
	else
	{
		if (percent < 0) 
			{return '↓ ' + ToText(Truncate(percent,1)) + ' % MTM';}
		else 
			{return ToText(Truncate(percent,1 )) + ' % MTM'}
	}

# All tables and charts based on Query where the last month’s data is selected.

## Full Version table

_This table show distribution of total installs by IRIS versions._

Table with Name and m_Count_sum in Display, no Group, Filter in Query.

## Name Table

_This table show distribution of total installs by apps._

Table with SystemVersionNumber and m_Count_sum in Display, no Group, Filter in Query.

## Country table

_This table show distribution of total installs by countries._

Table with Country and m_Count_sum in Display, no Group, Filter in Query.

## OS chart

_This chart show distribution of total installs by OS._

Pie chart with m_Count_sum in Show Values and SystemVersionOs in Category.


## Container chart

_This chart show distribution of total installs by types of installation._

Pie chart with m_Count_sum in Show Values and Container in Category.

# List 2

_On this page we have data about activity last month related to the 2021 IRIS version._

## Total installs

_Amount of total installs of IRIS 2021 applications._

Label displaying the parameter based on m_Count_sum from which the last month’s data is selected and SystemVersionNumber contains 2021. At the bottom of the label there is a label with data for the last 2 month. It displays a formula for displaying the name of the month and the parameter. The parameter is a copy of the one described above, but for a different period of time. 

## Total modules

_Amount of distinct IRIS 2021 applications that have been installed._

Label displaying the parameter based on m_Name_distinct  from which the last month’s data is selected and SystemVersionNumber contains 2021. At the bottom of the label there is a label with data for the last 2 month. It displays a formula for displaying the name of the month and the parameter. The parameter is a copy of the one described above, but for a different period of time. 

## Total hosts

_Amount of distinct ip addresses from which IRIS 2021 applications were installed._

Label displaying the parameter based on m_IP_distinct from which the last month’s data is selected and SystemVersionNumber contains 2021. At the bottom of the label there is a label with data for the last 2 month. It displays a formula for displaying the name of the month and the parameter. The parameter is a copy of the one described above, but for a different period of time. 

## MTM formulas and YTY formulas

	number percent;
	number @now = parameter displayed above formula.
	number @last = parameter similar to displayed above formula but for last 2 months or last year
	//In all formulas, parameters are used directly in the formula, without additional assignment to variables. This assignment is shown to understand how the formula works.
	percent = (@now - @last) / @last *100;
	if (percent > 0) 
		{return '↑ '+ ToText(Truncate(percent,1))+ ' % MTM';}
	else
	{
		if (percent < 0) 
			{return '↓ ' + ToText(Truncate(percent,1)) + ' % MTM';}
		else 
			{return ToText(Truncate(percent,1 )) + ' % MTM'}
	}

# All tables and charts based on Query that are filtered by MajorVersion (MajorVersion like 2021%) and the last month’s data is selected.

## Full Version table

_This table show distribution of total installs by IRIS 2021 versions._

Table with Namer and m_Count_sum in Display, no Group, Filter in Query.

## Name Table

_This table show distribution of total installs by apps with IRIS 2021 version._

Table with SystemVersionNumber and m_Count_sum in Display, no Group, Filter in Query.

## Country table

_This table show distribution of total installs of apps with IRIS 2021 version by countries._

Table with Country and m_Count_sum in Display, no Group, Filter in Query.

## OS chart

_This chart show distribution of total installs of apps with IRIS 2021 version by OS._

Pie chart with m_Count_sum in Show Values and SystemVersionOs in Category.

## Container chart

_This chart show distribution of total installs of apps with IRIS 2021 version by types of installation._

Pie chart with m_Count_sum in Show Values and Container in Category.

# List 3
_On this page we have all data about activity last month related to the 2021 IRIS version and installations in Docker containers._

## Total installs

_Amount of total installs of IRIS 2021 applications in Docker containers._

Label displaying the parameter based on m_Count_sum from which the last month’s data is selected, SystemVersionNumber contains 2021 and Container equal to “Docker”. At the bottom of the label there is a label with data for the last 2 month. It displays a formula for displaying the name of the month and the parameter. The parameter is a copy of the one described above, but for a different period of time. 

## Total modules

_Amount of distinct IRIS 2021 applications that have been installed in Docker containers._

Label displaying the parameter based on m_Name_distinct  from which the last month’s data is selected, SystemVersionNumber contains 2021 and Container equal to “Docker”. At the bottom of the label there is a label with data for the last 2 month. It displays a formula for displaying the name of the month and the parameter. The parameter is a copy of the one described above, but for a different period of time. 

## Total hosts

_Amount of distinct ip addresses from which IRIS 2021 applications were installed in Docker containers._

Label displaying the parameter based on m_IP_distinct from which the last month’s data is selected, SystemVersionNumber contains 2021 and Container equal to “Docker”. At the bottom of the label there is a label with data for the last 2 month. It displays a formula for displaying the name of the month and the parameter. The parameter is a copy of the one described above, but for a different period of time. 

## MTM formulas and YTY formulas

	number percent;
	number @now = parameter displayed above formula.
	number @last = parameter similar to displayed above formula but for last 2 months or last year
	//In all formulas, parameters are used directly in the formula, without additional assignment to variables. This assignment is shown to understand how the formula works.
	percent = (@now - @last) / @last *100;
	if (percent > 0) 
		{return '↑ '+ ToText(Truncate(percent,1))+ ' % MTM';}
	else
	{
		if (percent < 0) 
			{return '↓ ' + ToText(Truncate(percent,1)) + ' % MTM';}
		else 
			{return ToText(Truncate(percent,1 )) + ' % MTM'}
	}

# All tables and charts based on Query that are filtered by MajorVersion (MajorVersion like 2021%) and the last month’s data is selected, SystemVersionNumber contains 2021 and Container equal to “Docker”.

## Full Version table

_This table show distribution of total installs in Docker containers by IRIS 2021 versions._
 
Table with Namer and m_Count_sum in Display, no Group, Filter in Query.

## Name Table

_This table show distribution of total installs in Docker containers by apps with IRIS 2021 version._

Table with SystemVersionNumber and m_Count_sum in Display, no Group, Filter in Query.

## Country table
_This table show distribution of total installs of apps with IRIS 2021 version in Docker containers  by countries._

Table with Country and m_Count_sum in Display, no Group, Filter in Query.

## OS chart

_This chart show distribution of total installs  of apps with IRIS 2021 version in Docker containers by OS._

Pie chart with m_Count_sum in Show Values and SystemVersionOs in Category.

## Container chart

_This chart show distribution of total installs of apps with IRIS 2021 version in Docker containers by types of installation._

Pie chart with m_Count_sum in Show Values and Container in Category.

# List 4
_On this page we have all data about activity at last month related to only the 2021 IRIS version and installations directly on server OS._

## Total installs

_Amount of total installs of IRIS 2021 applications directly on server OS._

Label displaying the parameter based on m_Count_sum from which the last month’s data is selected, SystemVersionNumber contains 2021 and Container equal to “Server”. At the bottom of the label there is a label with data for the last 2 month. It displays a formula for displaying the name of the month and the parameter. The parameter is a copy of the one described above, but for a different period of time. 

## Total modules

_Amount of distinct IRIS 2021 applications that have been installed directly on server OS._

Label displaying the parameter based on m_Name_distinct  from which the last month’s data is selected, SystemVersionNumber contains 2021 and Container equal to “Server”. At the bottom of the label there is a label with data for the last 2 month. It displays a formula for displaying the name of the month and the parameter. The parameter is a copy of the one described above, but for a different period of time. 

## Total hosts

_Amount of distinct ip addresses from which IRIS 2021 applications were installed directly on server OS._

Label displaying the parameter based on m_IP_distinct from which the last month’s data is selected, SystemVersionNumber contains 2021 and Container equal to “Server”. At the bottom of the label there is a label with data for the last 2 month. It displays a formula for displaying the name of the month and the parameter. The parameter is a copy of the one described above, but for a different period of time. 

## MTM formulas and YTY formulas

	number percent;
	number @now = parameter displayed above formula.
	number @last = parameter similar to displayed above formula but for last 2 months or last year
	//In all formulas, parameters are used directly in the formula, without additional assignment to variables. This assignment is shown to understand how the formula works.
	percent = (@now - @last) / @last *100;
	if (percent > 0) 
		{return '↑ '+ ToText(Truncate(percent,1))+ ' % MTM';}
	else
	{
		if (percent < 0) 
			{return '↓ ' + ToText(Truncate(percent,1)) + ' % MTM';}
		else 
			{return ToText(Truncate(percent,1 )) + ' % MTM'}
	}

# All tables and charts based on Query that are filtered by MajorVersion (MajorVersion like 2021%) and the last month’s data is selected, SystemVersionNumber contains 2021 and Container equal to “Server”.

## Full Version table

_This table show distribution of total installs directly on server OS by IRIS 2021 versions._
 
Table with Namer and m_Count_sum in Display, no Group, Filter in Query.

## Name Table

_This table show distribution of total installs directly on server OS  by apps with IRIS 2021 version._

Table with SystemVersionNumber and m_Count_sum in Display, no Group, Filter in Query.

## Country table

_This table show distribution of total installs directly on server OS of apps with IRIS 2021 version by countries._

Table with Country and m_Count_sum in Display, no Group, Filter in Query.

## OS chart

_This chart show distribution of total installs  of apps with IRIS 2021 version directly on server OS by OS._

Pie chart with m_Count_sum in Show Values and SystemVersionOs in Category.

## Container chart

_This chart show distribution of total installs of apps with IRIS 2021 version directly on server OSby types of installation._

Pie chart with m_Count_sum in Show Values and Container in Category.
 
# List 5
_On this page we have charts that represent installation data for the last half a year._

All  charts based on Query where the last month’s data is selected.

## Installs Monthly bar chart

_This chart shows the number total installs._

Chart has m_Count_sum_summary in Show Values. m_Count_sum_summary is the summary of m_Count_sum group by TopName.

## Top applications installs bar chart

_This chart shows distribution of total installs by 10 most popular applications. ZPM on chart represents all other applications._

Chart has CountByTopName in Show Values and months in Series. Groups are swapped. CountByTopName is the summary of m_Count_sum group by months.

# List 6
_On this page we have charts that represent installation data for the last half a year._

All  charts based on Query where the last month’s data is selected 

## Containers vs Servers bar chart

_This chart shows distribution of total installs by installation type (Docker container or server OS)._

Chart has CountContainer in Show Values and months in Series. Groups are swapped. CountContainer is the summary of m_Count_sum group by Container.

## Hosts Monthly bar chart

_This chart shows the number of ip addresses on which applications were installed._

Shart has m_Ip_distinct in Show Values and months in Category.