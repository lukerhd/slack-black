# slack-black
Black theme for Slack

##Update for Slack 3.3.6
The latest update for Slack has likely blown out the appended data to the ssb-interop.js, it's also updated some structure/classes. Please use the following url:
https://raw.githubusercontent.com/lukerhd/slack-black/master/css/slack-black-3.3.6.css

Full snippet to append for Slack 3.3.6
document.addEventListener('DOMContentLoaded', function() {
 $.ajax({
   url: 'https://raw.githubusercontent.com/lukerhd/slack-black/master/css/raw/slack-black.css',
   success: function(css) {
     $("<style></style>").appendTo('head').html(css);
   }
 });
});

Similarly, with this theme you'd just append the following to /Applications/Slack.app/Contenst/Resources/app.asar.unpacked/src/static/ssb-interop.js:

document.addEventListener('DOMContentLoaded', function() {
 $.ajax({
   url: 'https://raw.githubusercontent.com/lukerhd/slack-black/master/css/raw/slack-black.css',
   success: function(css) {
     $("<style></style>").appendTo('head').html(css);
   }
 });
});
