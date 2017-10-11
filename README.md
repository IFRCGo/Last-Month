# Simple IFRC Go Page: DREFs & Appeals Last Month
Tableau dashboard with an overview of all DREFs and Appeals launched during the previous calendar month. Mainly to be used in monthly reporting.

## Use as a Template
This repository can be forked or cloned to create a new subpage.

1. Clone the repository
2. Rename Repository Name to the url wanted after ifrcgo.org (for this page it's "lastmonth"), giving the page the address http://ifrcgo.org/lastmonth/.
3. Go to Settings and set the source of GitHub Pages to "master branch"
4. Edit the index.html file

## Tableau Dashboards
If you want to simply create another page with another public Tableau dashboard, you only need to edit two lines of code:

### 1. HTML Title
The [HTML title](https://www.w3schools.com/tags/tag_title.asp). Set it to something fairly descriptive without being too long. End with " - IFRC Go" to show it's a page on Go.
```html
<title>DREFs & Appeals Last Month - IFRC Go</title>
```

### 2. Tableau Script
The [Tableau Script](https://onlinehelp.tableau.com/current/api/js_api/en-us/JavaScriptAPI/js_api_ref.htm). If you're not sure what to do here, simply change the `url` to the address of your new dashboard.
```html
<script type="text/javascript">
function initViz() {
  var containerDiv = document.getElementById("vizContainer"),
  url = "https://public.tableau.com/views/Operations2017/Dashboard2",
  options = {
    hideTabs: true,
    hideToolbar: false,
    display_count: false,
    showShareOptions: true,
    showVizHome: false,
    showAppBanner: false,
    onFirstInteractive: function () {
      console.log("Run this code when the viz has finished loading.");
    }
  };

  var viz = new tableau.Viz(containerDiv, url, options);
  // Create a viz object and embed it in the container div.
}
</script>
```
