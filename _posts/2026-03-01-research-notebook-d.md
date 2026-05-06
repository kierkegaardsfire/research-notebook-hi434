---
layout: post
title: "Research Notebook D"
date: 2026-03-01
---
<style>
/* Make the background image cover the ENTIRE browser window,
   not just the post content area */
body.notebook-d-bg {
  background-image: url("{{ '/assets/images/coins.png' | relative_url }}");
  background-size: cover;
  background-position: center top;
  background-attachment: fixed;
  background-repeat: no-repeat;
}

/* Dark overlay that also covers the entire viewport */
body.notebook-d-bg::before {
  content: "";
  position: fixed;
  top: 0; left: 0; right: 0; bottom: 0;
  background: rgba(0, 0, 0, 0.40);
  z-index: 0;
  pointer-events: none;
}

/* Make Minima's wrapper transparent so the image shows through */
body.notebook-d-bg .site-header,
body.notebook-d-bg .page-content,
body.notebook-d-bg .wrapper,
body.notebook-d-bg .site-footer {
  background: transparent !important;
  position: relative;
  z-index: 1;
}

/* Make the site nav text readable against the image */
body.notebook-d-bg .site-header {
  background: rgba(255, 255, 255, 0.92) !important;
}

body.notebook-d-bg .site-footer {
  background: rgba(255, 255, 255, 0.92) !important;
  color: #1a1a1a;
}

/* The translucent white panel for post content */
.bg-content-panel {
  position: relative;
  z-index: 1;
  max-width: 760px;
  margin: 30px auto;
  background: rgba(255, 255, 255, 0.88);
  padding: 40px 50px;
  border-radius: 4px;
  box-shadow: 0 4px 20px rgba(0, 0, 0, 0.3);
  backdrop-filter: blur(2px);
  -webkit-backdrop-filter: blur(2px);
}

.bg-content-panel,
.bg-content-panel p,
.bg-content-panel li,
.bg-content-panel h1,
.bg-content-panel h2,
.bg-content-panel h3 {
  color: #1a1a1a;
}

.bg-content-panel img {
  max-width: 100%;
  height: auto;
}
</style>

<script>
// Apply the background class to the body so the image covers the whole page
document.body.classList.add('notebook-d-bg');
</script>

<div class="bg-content-panel">
  
For my RAWGraph project I went online to find sample data because my own data wasn’t suited for this yet. I found a large excel file with thousands of rows of data mimicking the personnel list of a major company. Each person in the file had a variety of information about them, their Job Title, Department, Gender, Ethnicity, Age, Salary. Originally, my idea was to visualize the correlation between age and salary in the company. I figure this would show a clear correlation between the two, with average salary throughout the company rising with age. I initially wanted to do a bar graph before I spoke with Professor Carty, who suggested a scatter plot instead. With a scatterplot not being offered by RAWGraphs, I figured that a line graph would be the next best option. I put my data into the line graph, with age on the x axis and salary on the Y.

Here I ran into a problem, as RAWGraphs was categorizing my salary data as if it was qualitative, not quantitative. After googling I realized that this was because of the “$” in the dataset. So, I opened my original dataset in Google Sheets and attempted to get rid of the dollar sign. First I tried using the “search and replace” tool, but that was not working. The dollar signs remained there inexplicably. Some more research revealed that this was because it was a formatting issue, and the solution was to find the “number format” setting within Sheets. I turned off the “automatic” formatting, which removed the dollar sign. Then I downloaded the Sheet file as a new CSV, and started over in a new RAWGraphs.
Having resolved this problem, I was free to create my line graph. However, this did not turn out as I expected
As you can see, there was not the correlation I anticipated, although the very highest salary was indeed also one of the highest ages. I am not sure if the dataset I got was generated somehow, or if it was taken from real corporate data and anonymized in some way. In any case, I decided to look at other variables to try. I thought about swapping out “age” for “department” to see any pay disparity between the 7 divisions of the company: IT, Engineering, Sales, HR, Finance, Accounting, and Marketing. The results here, while not shocking, were more satisfying:
I sorted the bars in ascending order for better visualization. The results showed that marketing led the pack with an average salary of about $130,000, while IT trailed behind their co-workers, coming in at just under $100,000. 

</div>
