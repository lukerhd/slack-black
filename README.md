# slack-black
Black theme for Slack

Similarly, with this theme you'd just append the following to /Applications/Slack.app/Contenst/Resources/app.asar.unpacked/src/static/ssb-interop.js:

document.addEventListener('DOMContentLoaded', function() {
 $.ajax({
   url: 'https://raw.githubusercontent.com/lukerhd/slack-black/master/css/raw/slack-black.css',
   success: function(css) {
     $("<style></style>").appendTo('head').html(css);
   }
 });
});
