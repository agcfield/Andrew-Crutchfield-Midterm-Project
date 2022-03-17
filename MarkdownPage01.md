# IT Professions

![alt image](https://careertechnical.edu/wp-content/uploads/2019/09/IT-Professional-Reasons.jpg)

For this midterm project, I thought it would be appropriate to dedicate at least one markdown page to content that is relevant to this class. Therefore, this page is dedicated to *different* professions within the field of IT and information about them.
### List of Occupations

The following is a list of the four **highest** paying IT professions according to the [U.S. Bureau of Labor Statistics](https://www.bls.gov/ooh/computer-and-information-technology/home.htm) website. Click [here](https://comptiacdn.azureedge.net/webcontent/images/default-source/researchreports/it-industry-outlook-2022/report-chart-1_tech-occupation-employment-outlook.jpg?sfvrsn=f9a0f5e7_2) to see a graph showing projected employment growth for tech occupations.

1. Computer and Information Research Scientists
2. Computer Network Architects
3. Software Developers, Quality Assurance Analysts, and Testers.
4. Information Security Analyst

### Example of JavaScript Code

To demonstrate what *I* have learned so far in my IT education, here is a **very** simple JavaScript program that will print all of the even numbers appearing in a range of 1-100.

```
<!DOCTYPE html>
<html>
<head>
<meta charset="UTF-8">
<title>Even Numbers</title>
<script>

function showEvenNumbers() {
	var display = document.getElementById('display');
	var displayHTML = "";
	for (var i = 1; i < 101; i++) {
		if (i % 2 == 0) displayHTML += "<p>" + i + "</p>";
	}
	display.innerHTML = displayHTML
}

</script>

</head>

<body onload="showEvenNumbers()">
<div id="display">

</div>
</body>

</html>
```