# TechnicalQuestions
preparing for techinical interview


<!-- 
   Update: See the full example at https://github.com/dzello/preview_markdown_locally

   Slap this README.html next to your README.md and run under a web server.
   Dependencies are lib/require.js, lib/text.js and lib/markdown.js
   require.js and text.js are available at the require-js github repo: https://github.com/jrburke/requirejs
   Here I'm using the markdown.js from https://github.com/evilstreak/markdown-js
   Caveat - You might see slight differences when rendered on github due to GFM.
   Caveat 2 - file:// paths won't work because the README.md is loaded via the require-js text plugin.
 -->

<!DOCTYPE html>
<html>
<head>
  <link href="http://a248.e.akamai.net/assets.github.com/stylesheets/bundle_github.css"
        rel="stylesheet" type="text/css">
  <script src='require.js' type='text/javascript'></script>
  <script src='markdown.js' type='text/javascript'></script>
</head>
<body id="readme">
<div id="markdown" class="wikistyle"></div>
<script type="text/javascript">
  require({paths:{text:"lib/text"}}, ["text!README.md"], function(readme) {
    document.getElementById("markdown").innerHTML = markdown.toHTML(readme);
  });
</body>
</html>
